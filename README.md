# Postgresqk

## User

> O campo user define qual usuário irá ser usado para rodar os processos
> dentro do container. O usuário dump já existe dentro do container com o uid 1000

```shell
user: "dump"
```

## Build images

```shell
# base
docker build -t dumptec/postgresql:base-16.0-alpine3.18 -f Dockerfiles/16.0-alpine3.18/base/Dockerfile ./Dockerfiles/16.0-alpine3.18/base

# development
docker build -t dumptec/postgresql:dev-16.0-alpine3.18 -f Dockerfiles/16.0-alpine3.18/dev/Dockerfile ./Dockerfiles/16.0-alpine3.18/dev/

# production
docker build -t dumptec/postgresql:16.0-alpine3.18 -f Dockerfiles/16.0-alpine3.18/prod/Dockerfile ./Dockerfiles/16.0-alpine3.18/prod/

```

## Arquivos de configuração

> A configuração fica no caminho abaixo

* /usr/local/share/postgresql/postgresql.conf.sample
