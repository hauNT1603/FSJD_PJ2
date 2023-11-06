# Project 2 - FullStack JS - Udacity-build-a-storefront-backend
Build a JavaScript API based on requirements.


## Installation Instructions:
Install packages used in this project and how to install them.
`npm i`


Install packages db-migration with global flag.
`npm i -g db-migrate`


## Environmental Variables Set up

Create `.env` file in root directory if it not exists
```
POSTGRES_HOST=localhost
POSTGRES_DB=dev_db
POSTGRES_TEST_DB=test_db
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres123!
ENV=dev
BCRYPT_PASSWORD=thanhnhm
SALT_ROUNDS=10
TOKEN_SECRET=thanhnhm123

```

### Format

`npm run format` to run prettier


### Create Databases and Migrations

CREATE DATABASE dev_db;
CREATE DATABASE test_db;

`npm run dev-migrations; npm run test-migrations;`


### Start

`npm run start` to start the app and get access via http://localhost:3000:


### Test

`npm run test` to test


## Endpoint Access

All endpoints are described in the [REQUIREMENT.md](REQUIREMENTS.md) file.

## Token and Authentication

Tokens are passed along with the http header as

```
Authorization   thanhnhm123 eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VyIjp7ImlkIjoiNiIsInVzZXJuYW1lIjoidGhhbmhuaG0iLCJmaXJzdG5hbWUiOiJuZ3V5ZW4iLCJsYXN0bmFtZSI6InRoYW5oIiwicGFzc3dvcmRfZGlnZXN0IjoiJDJiJDEwJDlKNU1rZmFpdkx0RG5mY0xndkRLdGV0ejNTbXN1LzlmRUdSbVB4ZEtVWHhzcXc0azh2aDdLIn0sImlhdCI6MTY5OTE5ODg0Mn0.qPmXbbZmq6m_mmOg35D3DRr8ZVjZitO_q3K_iSB6dl8
```