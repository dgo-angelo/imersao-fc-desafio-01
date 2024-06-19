<p align="left">
  <img src="https://img.shields.io/static/v1?label=Typescript&message=language&color=red&style=for-the-badge&logo=typescript"/>
</p>
<p align="left">
  <img src="https://img.shields.io/static/v1?label=NODEJS&message=back-end&color=green&style=for-the-badge&logo=node.js"/>
</p>  
<p align="left">
  <img src="https://img.shields.io/static/v1?label=nestjs&message=framework&color=purple&style=for-the-badge&logo=nestjs"/>
</p>

### Tópicos

:small_blue_diamond: [Sobre o Projeto](#star-sobre-o-projeto)

:small_blue_diamond: [Funcionalidades](#bookmark_tabs-funcionalidades)

:small_blue_diamond: [Como rodar a aplicação](#arrow_forward-como-rodar-a-aplicação)

## :star: Sobre o Projeto

Aplicação desenvolvida para resolução do desafio "Criando API de reserva de ingressos com Nest.js - 
Fase 01", da [Imersão Full Stack & Full Cycle](https://imersao.fullcycle.com.br/evento/).

Este projeto foi desenvolvido utilizando:

:heavy_check_mark: NodeJS

:heavy_check_mark: NestJS

:heavy_check_mark: Prisma ORM + MySQL

:heavy_check_mark: Docker

## :bookmark_tabs: Funcionalidades

A lista das apis e como utiliza-las encontra-se no arquivo ```api.http```, deste projeto.


## :arrow_forward: Como rodar a aplicação

#### :heavy_check_mark: Clonando o Projeto

- No terminal, clone o projeto:

  ```
  https://github.com/dgo-angelo/imersao-fc-desafio-01
  ```

### :arrow_forward: Executando a aplicação

- Acessar a pasta raiz do projeto e executar o comando, baixo, responsável pela criação do container docker com banco de dados mysql

```
docker-compose up -d
```

- Acessar a pasta raiz do projeto e instalar as dependencias através do comando:

```
npm install
```

- Será necessário criar o arquivo .env, utilizado pelo Prisma:

```
DATABASE_URL="mysql://usuario:senha@localhost:porta/banco"
API_TOKEN="INFORMAR O TOKEN DE SEGURANÇA UTILIZADO PELO AUTHGUARD APIS"
```

- Executar o comando para sincronização do schema com o banco de dados:

```
npx prisma db push
```

- Agora você está pronto para iniciar a aplicação:

```
npm run start:dev
```