#  Chapter III - Desafio 01: Database Queries :rocket: :purple_heart:

## :dart: Objetivo

Realizar consultas no banco de dados com o TypeORM de três formas:

- ORM
- Query Builder
- Raw Query

## :white_check_mark: Requisitos

### Repositórios da aplicação

#### UsersRepository
- [x] findUserWithGamesById
- [x] findAllUsersOrderedByFirstName
- [x] findUserByFullName

#### GamesRepository
- [x] findByTitleContaining
- [x] countAllGames
- [x] findUsersByGameId

### Específicação dos testes

#### UsersRepository
- [x] Should be able to find user with games list by user's ID
- [x] Should be able to list users ordered by first name
- [x] Should be able to find user by full name

#### GamesRepository
- [x] Should be able find a game by entire or partial given title
- [x] Should be able to get the total count of games
- [x] Should be able to list users who have given game id

## :computer: Instalação ##

```bash
# Clone este repositório
$ git clone https://github.com/leandrolimadeveloper/desafio-database-queries-ignite.git

# Entre na pasta
$ cd desafio-database-queries-ignite

# Instale as dependências
$ npm i
```

## Execução dos testes
Para rodar os testes é necessário ter o Docker instalado, e ter uma imagem do PostgreSQL.
```bash
# Com o Docker em execução, crie uma base de dados chamada queries_challenge com o comando:
$ docker run --name ignite-challenge-database-queries -e POSTGRES_DB=queries_challenge -e POSTGRES_PASSWORD=docker -p 5432:5432 -d postgres

# Para verificar se o container está rodando:
$ docker ps 

# Se o container estiver em execução, na pasta em que está localizado o projeto, execute:
$ npm run test
```

Após finalizar os testes, execute no terminal para encerrar o container:
```bash
$ docker stop ignite-challenge-database-queries
```

Caso também prefira excluir o container, execute:
```bash
# Listar os containers 
$ docker ps -a

# Excluir container (com id ou nome do container)
$ docker rm id/ignite-challenge-database-queries
```
