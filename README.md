<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src=".github/logo.png" width="300px" border-radius:"5px" />
</h1>

<h3 align="center">
  Front-end web: Rocketshoes
</h3>

<p>Esse projeto é referente ao módulo 7 da 10º edição do Bootcamp GoStack da Rocketset. </p>

## Sobre o desafio

**RocketShoes** é uma aplicação de logística, feito com o intuíto de auxiliar no gerenciamento e no controle das entregas de encomendas.

Esse auxílio é feito através de ferramentas que permitem, ao administrador, o cadastro de entregadores, destinatários e encomendas; a associação destas encomendas aos entregadores que, por sua vez, administram suas entregas através do aplicativo mobile; e o gerenciamento dos problemas ocorridos nas entregas possibilitando, eventualmente, o cancelamento das mesmas.

No aplicativo mobile, o entregador tem acesso às encomendas atribudas a ele (pendentes e já concluídas); tem os recursos de confirmação de retirada de encomenda e de entrega conclúida (atestada por uma foto da assinatura do destinatário); e, também, a possibilidade de cadastrar um problema com uma entrega especfica e visualizar o histórico de problemas atribuídos.

As tecnologias utilizadas no desenvolvimento, foram: **Node.js**, **ReactJS** e **React Native**.

<p align="center">
  <img alt="Rocketshoes_main" title="Rocketshoes_main" src=".github/rocketshoes_main.png" width="100%" />
  <img alt="Rocketshoes_cart" title="Rocketshoes_cart" src=".github/rocketshoes_cart.png" width="100%" />
</p>

## Back-end

Para executar o back-end é preciso acessar, via terminal, a pasta `backend` e seguir os seguintes passos:

**1.** Criar containers de Postgres e Redis no Docker, com o comando:

`docker run --name db_fastfeet -e POSTGRES_PASSWORD=docker -p 5433:5432 -d postgres`

e

`docker run --name redisfastfeet -p 6380:6379 -d -t redis:alpine`

**2.** Iniciar bancos de dados no Docker, com o comando: 

`docker start db_fastfeet redisfastfeet`

**3.** Gerar as tabelas no banco de dados, através das migrations e seeds do Sequelize, com os comandos:

`yarn sequelize db:migrate` e `yarn sequelize db:seed:all`

**4.** Configurar o MailTrap no arquivo `web/src/config/mail.js` com o `user` e `pass` da sua conta.

**5.** Finalmente, executar o comando `yarn dev` para rodar a api.

## Web

Para executar a aplicação web você deve acessar, via terminal, a pasta `web` e executar: `yarn start`.

