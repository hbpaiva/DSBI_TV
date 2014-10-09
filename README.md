DSBI_TV
=======

Repositório Henrique e Juliana

**************************************************************************************************
 Se quiser selecionar apenas a coluna é só no lugar do asterisco os nomes
***************************************************************************************************

proc sql;
connect to hadoop (user = "hadoop" pw="hadoop" server="10.238.10.40" port = 10010 
cfg="/sas93/hadoop/conf2.xml" schema=d_bigd_db READ_METHOD=HDFS);
select * from connection to hadoop (
select 
*
from
tbgdt_wrk_dpi_fat limit 100);
disconnect from hadoop;
quit;
