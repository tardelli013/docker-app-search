
## Este é o projeto backend + database para consultas por `name` e `usename` rodando no Docker


## Requisitos para rodar o projeto
- Docker + Docker-Compose

## Stack
- Docker
- Java
- Spring Boot
- Maven
- Swagger
- ElasticSearch
- NGINX

## Run
- É necessário copiar o arquivo users.csv para `app/src/main/resources/database` este arquivo .csv será carregado no ElasticSearch em background
- O arquivo possui cerca de 600 MB e pode ser baixado [aqui](https://drive.google.com/file/d/1fp7EUL0uVtnHmPUvPjFIUEZfvivwJKlJ/view?usp=sharing)
- Ao iniciar a aplicação, em background este arquivo é carregado e a API já pode ser utilizada porém não com a totalidade dos registros, em testes em uma máquina com Ubuntu, 8GB ram e Processador I5 a carga completa demorou 10 horas.

- Para rodar o ElasticSearch é necessário alterar o max_map_count no linux: `sudo sysctl -w vm.max_map_count=262144`

- O comando abaixo sobe as imagens docker do NGINX, ElasticSearch e SpringBoot
- Run command `docker-compose up`

- Ao final do build o console exibirá a mensagem a seguir:  Swagger running in: http://localhost/swagger-ui.html

- Acessse o endereço http://localhost/swagger-ui.html para ver a documentação da API no Swagger

