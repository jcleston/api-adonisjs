<p align="center">
  <img alt="Repository size" src="https://img.shields.io/github/repo-size/jcleston/api-adonisjs">
  <a href="https://github.com/jcleston/api-adonisjs/commits/main">
    <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/jcleston/api-adonisjs">
  </a>
   <a href="https://github.com/jcleston/api-adonisjs/stargazers">
    <img alt="Stargazers" src="https://img.shields.io/github/stars/jcleston/api-adonisjs?style=social">
  </a>
  <a href="https://www.linkedin.com/in/janescleston/">
    <img alt="Feito por Janes Cleston" src="https://img.shields.io/badge/feito%20por-Janes%20Cleston-%237519C1">
  </a>
</p>

## Menu Geral
<!--ts-->
* [Instalação](#instalação)
  * [Comandos](#comandos)
* [Desenvolvimento](#desenvolvimento)
  * [Model](#model)
  * [Migration](#migration)
  * [Controller](#controller)


<!--te-->
<br /><br />

## Instalação
Atualizando o nodejs

```shell
$ sudo npm install -g n
$ sudo n latest
$ sudo n stable
```

Instalando o adonisjs

```shell
$ npm init adonis-ts-app@latest api-adonisjs
```

Iniciando o server
```shell
$ node ace serve --watch
```

Instalando e configurando o lucid
```shell
$ npm i @adonisjs/lucid
$ node ace configure @adonisjs/lucid
```
Editar o arquivo cors.ts
```shell
enabled: (request) => request.url().startsWith('/api'),
```

Editar o arquivo routes.ts
```shell
Route.group(() => {
  Route.get('/', async () => {
    return { hello: 'world' }
  })
}).prefix('/api')
```

Instalando o uuid

```shell
$ npm i uuid
```

## Comandos
```shell
Para ver todas as opções
$ node ace

Para ver as rotas disponiveis
$ node ace list:routes
```

<br /><br />

## Desenvolvimento
Iremos utilizar o padrão MVC

## Model
Para criar um model
```shell
$ node ace make:model Moment -m
$ node ace make:model Comment -m
```

## Migration
Para rodar a migration
```shell
$ node ace migration:run
```

## Controller
Para criar um controller
```shell
$ node ace make:controller Moment
```
