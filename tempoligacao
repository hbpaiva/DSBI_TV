DSBI_TV
=======

Repositório Henrique e Juliana
duracao<- function(x,colA,colB,colT){ ## inserir o dataframe, coluna do discador, coluna do recebedor, coluna de tempo de chamada
a=integer()
b=integer()
tempo=integer()
ocorrencias=integer()
nl=nrow(x)
f=1
j=1

while(j < nl){
		  k=1
		  a<-x[j,colA]
		  b<-x[j,colB]
		  c<-x[j,colT]
		  for(i in 1:nl){
					if(x[i,colA]==a){
							if(x[i,colB]==b){
									c[k]<-x[i,colT]
									k=k+1
									}}}
		 tempo[f]<-sum(c)
		 ocorrencias[f]<-k-1
		 f=f+1
		 j=j+1
		 }	
return(data.frame(soma,ocorrencias))
}
