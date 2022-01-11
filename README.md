# kubedev-desafio-microservico
Este é o desafio final do modulo de docker. O objetivo deste desafio é levantar uma aplicação que utiliza de micro serviços utilizando de 3 aplicações, cada aplicação possui suas particularidade como banco de dados específicos e desenvolvida com linguagem diferentes.
## Requisitos para o projeto
  - Trabalhar com arquivos de enviroment separada e dar liberdade para os desenvolvedores.
  - Todo o ambiente deve ser iniciada a partir de um único comando.
  - As imagem geradas tem que trabalhar sempre com a mesma versão.
  - Criar todo ambiente a partir de um Docker-compose.
## Diagrama do projeto 
![Diagrama do projeto](img/diagrama.png)
## Informações do projeto
  Este projeto é composto de três diretório cada diretório é um projeto separado.
  - movie
    - Aplicação responsável pelo catálogo dos filmes.
    - Aplicação desenvolvida em **node:17**
      - Porta *default* *8181*
      - Start pelo *server.js*
    - Necessita de banco NoSQL mongodb
  - review
    - Aplicação responsável pela informações 
    - Aplicação desenvolvida em **asp.net versão 5**
      - Deve rodar na porta *default* *8282*
      - Variável que define porta  asp.net *ASPNETCORE_URLS=http://+:8282*
    - Necessita do Banco SQL postgreSQL
  - rotten-potatoes-ms
    - Aplicação responsável pelo frontend.
    - Conecta via url nas aplicações de backend
    - Aplicação feito em python 3.10.1 com flask
      - Porta *default* do python 5000
## 
