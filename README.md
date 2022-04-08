# diabetes
Projeto previsão de pessoas com Diabetes


Participei de um projeto que fez uma analise de previsão com pessoas com diabetes, uma iniciativa da Stack Tecnologia, criou o programa Stack Labs, que simula um projeto real da área de dados.

Na Squad eu fiz o papel de Engenheiro de Dados, criando infra estrutura para tratamento do fluxo de dados, e disponibilizando para analise e criação do modelo final.

## Tecnologias Utilizadas

- Jupyter
- Visual Studio Code
- Docker
- Apache Airflow
- Mailtrap - Envio de email
- Cloud AWS
- Amazon S3
- RDS - Mysql Server
- EC2 - Streamlit

## Overview do Fluxo de Dados

<p align="center">
  <img src="https://github.com/villani31/diabetes/blob/main/Desenho_Projeto_Stacklabs.png" alt="Pipeline"height=400px >
</p>

## Entendendo o pipeline:

- Pego do site do Kaggle os Datasets disponíveis publicamente no link: https://www.kaggle.com/datasets/alexteboul/diabetes-health-indicators-dataset.
- Enviado para o repositório do Github.
- Criado um ambiente dentro da Cloud da AWS.
    - RDS (Banco de dados Mysql Server)
    - Amazon S3 (Data Lake)
    - Instancia EC2 (App Streamlit)
- Utilizando o Jupyter Notebook, criado uma conexão (engine), para leitura, entendimento dos dados, e importação dos datasets para tabelas dentro do banco de dados Mysql Server.
- Usando uma infra estrutura On-premise com Docker, criado um container com Apache Airflow.
- Com o Apache Airflow:
    - Desenvolvido um Pipeline, para carregar os Datsets a partir do Github, transformar em formato parquet, e envia para o serviço da Amazon S3 (Data Lake), no Satage01.
    - Após pegando os arquivos do Satage01, fazendo a limpeza, e consolidando os dados em apenas um dataset, enviando para o Stage02, disponibilizando os dados para o Cientista de Dados fazer analise e criar o modelo.
    - Criando o modelo final, sendo enviado para o Stage03, disponibilizando para a instancia EC2, carregar o App em Streamlit, a partir do modelo gerado.

## Conclusão

Um projeto muito desafiador, em pouco tempo, em conjunto com minha Squad que participei, entregar um projeto de dados completo, desde a Engenharia de Dados, Analise de Dados, Ciências de Dados, e a entrega do produto final, que foi o aplicativo auxilia em prever se a pessoa tem diabetes ou não.


