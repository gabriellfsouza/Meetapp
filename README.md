# MeetApp

![](https://img.shields.io/github/issues/gabriellfsouza/meet-app-back.svg) ![](https://img.shields.io/github/forks/gabriellfsouza/meet-app-back.svg) ![](https://img.shields.io/github/stars/gabriellfsouza/meet-app-back.svg) ![]()

### Introdução

Esta aplicação faz parte do deafio para o bootcamp da RocketSeact (fullstack javascript developer com ReactJS, React Native e NodeJS).
A ideia deste projeto é o desenvolvimento de uma aplicação para agendamento e
gerencimaento de Meetups.

A parte mobile deste projeto não foi testado para IOS, somente apara Android.

## Funcionalidades

- Manage alerts for products prices on Ebay.com to be sent to provided email;
- Each alert will be related with a search phrase and interval to send the email;
- Interval is a value in minutes and must have one of the following values:

```javascript
const interval = [2, 10, 30];
```

- The email must to have the first 3 products searched by the phrase, sorted by the lowest price;
- Several alerts can be created for the same email address byt with different search phrases;
- The UI(s) must to provide a list with all alerts registered and a CRUD interfaces;

#### Aditional Technologies Envolved

- MongoDB to maintain data;
- Redis to manage the email queue;
- Sentry to register production erros;
- Docker to containerize the solution and a docker-compose to run whole environment;
- TDD with Jest;
- Airbnb Style Guide;
- JSDocs

```javascript
/**
* Description
* @param {type} paramName
*/
function myFuntion(paramName){...}
```

### Ebay Search API

![](https://upload.wikimedia.org/wikipedia/commons/1/1b/EBay_logo.svg)

You need to create a client app account in eBay to obtain the App ID and use the search API at https://developer.ebay.com

## Pré requisitos

Para a execução deste projeto, é necessário ter o Docker instalado e para a parte do projeto Mobile deve-se configurar o ambiente conforme link abaixo:
https://docs.rocketseat.dev/ambiente-react-native/introducao
É possível também executar o projeto sem o docker, basta apontar o arquivo de configuração para o Redis e Postgres externo.

### Instancia dos conteineres

```
docker run --name mongo -p 27017:27017 -d -t mongo
docker run --name redis -p 6379:6379 -d -t redis:alpine
```

## Instalação

Baixe os 3 projetos (Back, Front e Mobile) e instale conforme abaixo:

### Back

```
git clone https://github.com/gabriellfsouza/meet-app-back
cd meet-app-back
yarn

```

### Front

```
git clone https://github.com/gabriellfsouza/meet-app-font
cd meet-app-back
yarn
```

### Mobile

```
git clone https://github.com/gabriellfsouza/meet-app-mobile
cd meet-app-back
yarn
```

### Arquivo .env

Todos os projetos possuem um arquivo ".env.example", que devem ser renomeados e utilizados como arquivo de configuração para as variáveis de ambiente, como conexão com a base, caminho da chamada http, etc.

### Execução

Tanto para a parte web quanto para a front, basta executar o comando abaixo:

```
yarn start
```

Para a versão Mobile, será necessário executar o comando abaixo:

```
react-native run-android
```

dica: para executar localmente (mobile), basta executar o comando abaixo

```
adb reverse tcp:3333 tcp:3333
```

Qualquer dúvida, pode entrar em contato comigo no e-mail gabriellfsouza@gmail.com
