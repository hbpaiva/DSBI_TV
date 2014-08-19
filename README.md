DSBI_TV
=======
Repositório Henrique e Juliana
topicos<-read.csv2("Tópicos - Cópia.txt", header=FALSE, colClasses="character")

lista <- function(topicos){

topicos2<-unlist(strsplit(topicos$V1,";"))
topicos3<-unlist(strsplit(topicos2,":"))
 
resultado<-data.frame(length(topicos2),2)
j=1
for(i in 1:nrow){
	
	##resultado[i,1]<-topicos3[j] (tirei a coluna que tinha os itens topics, por isso o ##)
	resultado[i,1]<-topicos3[j+1]
	resultado[i,2]<-topicos3[j+2]
	j=j+3
}

names(resultado)<-c("Número","Tópico")
resultado$Número<-as.numeric(resultado$Número)
resultado<-data.table(resultado[order(resultado$Número),])
return(unique(resultado)) ## Se precisar que apareça todas as repetições é só tirar o "unique"
}
