# grafana-influxdb-docker-starter

> A small docker-compose setup for a Grafana dashboard with InfluxDB

![GitHub Repo stars](https://img.shields.io/github/stars/vabarnabas/grafana-influxdb-docker-starter)
![GitHub forks](https://img.shields.io/github/forks/vabarnabas/grafana-influxdb-docker-starter)

This project could be useful to set up a dashboard for performance and load testing performances with K6, this is why the default database name is `k6`.

## Installation

Installation guide for Docker Compose: https://docs.docker.com/compose/install/

To start the project, run:

```sh
docker-compose up -d
```

## Usage example

By default the project was used for K6 Load Testing, so if you would like to change the database name you should change it in the `docker-compose.yml`:

```yml
environment:
  - INFLUXDB_DB=<YOUR_DATABASE_NAME>
```

And in the `grafana-datasource.yml`:

```yml
database: <YOUR_DATABASE_NAME>
```
