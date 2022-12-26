# Aplicação Web com Metrics e Prometheus 

## Projetos  
Temos três aplicações base para simular um ambiente monitorado

### WebSite
Uma aplicação Web em C# .Net Core Default, com Metrics configurado para conseguirmos monitorar através de um scrape do Prometheus.
Caso não saíba o que é um scrape sugiro olhar esse site aqui [Prometheus.IO](https://prometheus.io/docs/prometheus/latest/getting_started/)

Host: http://localhost

### Prometheus 
TODO 

Host: http://localhost:9090

### Grafana
Usuário e senha default na primeira execução  

Host: http://localhost:3000  
Usuário: admin  
Senha: admin  
*Necessário cadastrar uma senha no primeiro acesso;

Quando for adicionar o datasource do prometheus no grafana é necessário utilizar o IP do container (Não é a melhor forma, o ideal seria configurar o DNS)
Para obter o IP do container do Prometheus é necessário
 - listar todos os containers em execução no docker `docker ps`;
 - inspecionar o container do prometheus no docker `docker inspect [NAME DO CONTAINER DO PROMETHEUS]`
 - copiar o "IPAddress" do container do prometheus e utilizar o mesmo na configuração do datasource ex: http://172.26.0.3:9090

## Requisitos
TODO 

## Setup 
Para rodar todas as aplicações de uma vez basta exercutar o comando abaixo na raiz do projeto.  
`docker compose up -d`

### Autor 
David Coca
dtadeu.coca@gmail.com