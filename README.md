# PG Checker

A tool to test PostgreSQL connections. The mode of operation and other parameters are configured using a simple YAML configuration file.

## Build

`make build`

```bash
DATABASE_USER=username DATABASE_PASSWORD=super-password DATABASE_NAME=database-name DATABASE_HOST=my-pg-hostname.domain ./pg-checker
```

## Create docker image

```bash
TAG=master docker-build-image
```

## Upload docker image

```bash
TAG=master docker-push
```

## Using docker image

```bash
docker run --name pg-checker -e DATABASE_USER=XPTO -e DATABASE_PASSWORD=XPTO -e DATABASE_NAME=database-name -e DATABASE_HOST=my-pg-hostname.domain -e DATABASE_PORT=5432 ruancasas/pg-checker:main
```
