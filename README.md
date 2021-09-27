# **Teste Node.js Contele**

![](https://img.shields.io/badge/version-1.0-blue.svg) ![](https://img.shields.io/badge/language-Typescript-blue.svg) ![](https://img.shields.io/badge/license-GPL_V3-blue.svg)
![](https://img.shields.io/badge/author-Crisler-blue.svg)

## Tecnologias utilizadas

<div style="display: inline_block">
 <img height="50" width="50" alt="nestjs" src="https://cdn.jsdelivr.net/npm/simple-icons@3.12.1/icons/nestjs.svg" />&nbsp;&nbsp;&nbsp;&nbsp;
  <img height="50" width="50" alt="Typescript" src="https://cdn.jsdelivr.net/npm/simple-icons@3.12.1/icons/typescript.svg" />&nbsp;&nbsp;&nbsp;&nbsp;
  <img height="50" width="50" alt="docker" src="https://cdn.jsdelivr.net/npm/simple-icons@3.12.1/icons/docker.svg" />&nbsp;&nbsp;&nbsp;&nbsp;
  <img height="50" width="50" alt="postgresql" src="https://cdn.jsdelivr.net/npm/simple-icons@3.12.1/icons/postgresql.svg" />&nbsp;&nbsp;&nbsp;&nbsp;


## Dependencias Instaladas
- Typeorm 
- pg
- @nestjs/typeorm
- @nestjs/config


## Descrição

Esta aplicação foi desenvolvida para a vaga de desenvolvedor Node.js na Contele ao qual foit utilizado o framework Nestjs, ao qual tem por linguagem padrão Typescript. Tambem foi utilizado o Docker para o desenvolvimento e o banco de dados PostgreSQL.

## Como utilizar

- É necessário ter o Docker instalado juntamente com o Docker Compose.

Após clonar o repositório, dentro da pasta do projeto, são necessário executar os comando:

```
chmod +x .docker/entrypoint.sh
sudo docker-compose up --build
```
## Links
- Acesso ao endpoind da api: http://localhost:3002/subscription
- Acesso ao pgAdmin: http://localhost:9000
- Acesso ao frontend: http://localhost:3000
## Instruções
- Apos fazer o build da aplicação é necessário executar o comando:
 `sudo docker-compose exec app bash`
  e depois executar o comando:
  `npm run typeorm migration:run`

- Ao acessar o PgAdmin, utilize o usuario admin@user.com e a senha 123456.
Crie um server com o name db, host_name como db e usuario como postgres.

- Caso queira alterar, faça as modificações no arquivo docker-compose.yml
## Formato de dados a serem enviados

Application/json
```json
{
  "first_name": "Carlos",
  "last_name": "Rivera",
  "email": "carlosrivera@email.com",
  "phone_number": "5493433293",
  "first_adress": "Avenida das Lebres 343",
  "second_adress": "La Paz",
  "city": "mexico city",
  "state": "us",
  "zip_code": "73232-45",
  "language": "en",
  "country": "us",
  "billing_city": "mexico city",
  "billing_state": "us",
  "billing_zip_code": "73232-45",
  "primary_billing_adress": "Avenida das Lebres 343",
  "second_billing_adress": "La Paz",
  "fcut_device": true,
  "other_installed_trackers": true,
  "identify_fleet_drivers": true,
  "same_shipping_adress": true,
  "tracker_quantity": 8
}
```

## Formato dos dados retornados pelo serviço:

```json
{
  "id": 2,
  "first_name": "Carlos",
  "last_name": "Rivera",
  "email": "carlosrivera@email.com",
  "phone_number": "5493433293",
  "first_adress": "Avenida das Lebres 343",
  "second_adress": "La Paz",
  "city": "mexico city",
  "state": "us",
  "zip_code": "73232-45",
  "language": "en",
  "country": "us",
  "billing_city": "mexico city",
  "billing_state": "us",
  "billing_zip_code": "73232-45",
  "primary_billing_adress": "Avenida das Lebres 343",
  "second_billing_adress": "La Paz",
  "fcut_device": true,
  "other_installed_trackers": true,
  "identify_fleet_drivers": true,
  "same_shipping_adress": true,
  "tracker_quantity": 8,
  "created_at": "2021-09-25T12:11:16.750Z"
}
```
