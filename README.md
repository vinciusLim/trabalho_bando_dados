Neste trabalho, foi utilizado o Data Warehousing (DW) com as camadas Landing, Bronze, Silver e Gold, que são responsáveis por organizar e processar os dados de forma estruturada. Esse modelo é amplamente adotado em arquiteturas de Data Lakehouse, que combinam Data Lakes e Data Warehouses para permitir análises avançadas e eficientes.

A primeira camada, denominada Landing, recebe os dados brutos da fonte do github sem qualquer tipo de processamento ou transformação, preservando sua integridade original. Nesta etapa, os dados são ingeridos a partir de fontes como arquivos CSV.
Em seguida, na camada Bronze, os dados ainda permanecem quase brutos, mas passam por uma mudança de formato para otimizar o armazenamento e a manipulação, sendo convertidos para o formato Parquet.

Na camada Silver, ocorre um processo de refinamento e padronização dos dados, com a remoção de erros e duplicidades para garantir maior qualidade e confiabilidade. Alguns exemplos de transformações realizadas nesta etapa incluem a remoção de acentos e pontuações, a conversão de strings para uppercase e o tratamento de campos de CEP (zip_code) para exibição dos cinco primeiros dígitos, conversão da tipagem de dados, para String, Int, Double e outros.

Por fim, a camada Gold contém os dados prontos para o consumo analítico e a geração de relatórios executivos. Nesta etapa, a modelagem é otimizada para ferramentas de Business Intelligence (BI), formando tabelas fatos e duas dimensões.


Tabelas no postgres depois do loading

![alt text](image.png)