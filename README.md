## Desafio Backend Banco BTG Pactual

Este projeto é um desafio backend para o Banco BTG Pactual, implementado usando Java 17, Spring, Docker, MongoDB e RabbitMQ. O objetivo é criar um serviço de pedidos (`orderms`) que interage com RabbitMQ para gerenciamento de mensagens.

### Tecnologias Utilizadas

- ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white) **Java 17**
- ![Spring](https://img.shields.io/badge/Spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white) **Spring Boot**
- ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) **Docker**
- ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white) **MongoDB**
- ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=rabbitmq&logoColor=white) **RabbitMQ**

### Requisitos

- **Java 17** instalado
- **Docker** e **Docker Compose** instalados

### Estrutura do Projeto

- `src/main/java`: Contém o código fonte da aplicação.
- `src/main/resources`: Contém arquivos de configuração, como `application.properties`.
- `Dockerfile`: Dockerfile para construção da imagem da aplicação.
- `docker-compose.yml`: Arquivo para orquestração de containers Docker.


# Desafio Engenheiro de Software - BTG Pactual

## Instruções

- Leia esse documento com atenção antes de iniciar as atividades.
- Você tem **1 dia** para entregar o plano de trabalho (item 1).
- Você tem até **7 dias corridos** para concluir as atividades aqui solicitadas. Caso não consiga concluir todas as atividades, por favor, entregue o que foi feito até a data solicitada.
- Crie um repositório no Github para seu projeto e mantenha o seu projeto como público.
- Ao concluir as etapas de entrega, envie um e-mail, com o assunto "[DESAFIO BTG] - SEU NOME COMPLETO", para: ****@btgpactual.com.
- Fique à vontade para utilizar tecnologias, frameworks e técnicas não citadas nas atividades ou substituir as que julgar necessário. Informe em seu relatório as modificações e os motivos.
- A aplicação deve ser entregue “rodando”, com instruções para interagir com ela.
- Recomendamos a utilização do Docker (http://www.docker.com) para montagem do ambiente (MongoDb, RabbitMQ, Web Application, etc.). Caso opte pela utilização do Docker, crie uma única imagem com todos os containers e compartilhe em seu relatório final.

## Escopo

Processar pedidos e gerar relatório.

## Atividades

1. **Elabore e entregue um plano de trabalho.**
    - Crie suas atividades em tasks.
    - Estime horas.

2. **Crie uma aplicação** na tecnologia de sua preferência (JAVA, DOTNET, NODEJS).

3. **Modele e implemente uma base de dados** (PostgreSQL, MySQL, MongoDB).

4. **Crie um micro serviço que consuma dados de uma fila RabbitMQ** e grave os dados para conseguir listar as informações:
    - Valor total do pedido
    - Quantidade de Pedidos por Cliente
    - Lista de pedidos realizados por cliente

   Exemplo da mensagem que deve ser consumida:

   ```json
   {
       "codigoPedido": 1001,
       "codigoCliente":1,
       "itens": [
           {
               "produto": "lápis",
               "quantidade": 100,
               "preco": 1.10
           },
           {
               "produto": "caderno",
               "quantidade": 10,
               "preco": 1.00
           }
       ]
   }
