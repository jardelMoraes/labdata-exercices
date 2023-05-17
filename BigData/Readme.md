<div align="center">
  <img src="https://github.com/jardelMoraes/labdata-exercices/blob/main/BigData/Fluxo%20de%20dados.png" alt"Proffy" title="Proffy" alt"Proffy" title="Proffy" />
  </div>

**1) Definição do problema:** <br />
   Somos uma empresa de análise de dados que presta serviço para várias academias. <br />
        Com os dados das academias, pretendemos realizar várias análises de dados de cada uma pra tirar alguns insights de
            sazonalidade, padrão do perfil.<br /><br />
    **Problema:** Queremos captar os dados de várias academias separadas e mandar para nossa empresa para fazer as análises.<br />
 
**2) Definição da ingestão em dados:**<br />
    Cada academia tem seus bancos próprios (cada uma utiliza uma ferramenta diferente, SQL, excel...).<br />
    Nós vamos captar os dados das academias utilizando Airflow que irá ingerir os dados na empresa.<br />
    - Os dados já existem em cada uma das academias, iremos apenas captar utilizando o Airflow para ingerir dentro do nosso sistema.<br />
 
 **Origem:** Dados estão armazenados em cada academia.<br />
 **Ingestão:** Será realizada pelo Airflow via API, mandando um JSON.<br />
 
**3) Definição da arquitetura:**<br />
    - Armazenamento: Blob Storage para armazenamento dos dados brutos que recebemos em formato JSON/Imagem, pois é apenas para dados não estruturados <br />
 
**4) Camada de Processamento:**<br />
    - Azure HDInsight: Cluster que utiliza como motor ferramentas o Hive e o Spark, proporcionando um processamento tanto para batch quanto para streaming na cloud.
 
**5) Camada de Exploração:**<br />
    - Databricks: Ferramenta que permite a exploração dos dados, com a possibilidade de utilizar linguagens como Python, Scala, SQL, R, Java, etc. <br />
 
**6) Camada de Disponibilização:**<br />
    - Cosmos DB via API: Armazena os dados já processados e disponibiliza via API para o usuário final. 
