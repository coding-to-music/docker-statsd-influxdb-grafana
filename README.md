# docker-statsd-influxdb-grafana

# 🚀 Docker service with Telegraf (StatsD), InfluxDB and Grafana 🚀

https://github.com/coding-to-music/docker-statsd-influxdb-grafana

From / By Samuele Bistoletti https://github.com/samuelebistoletti

https://github.com/samuelebistoletti/docker-statsd-influxdb-grafana

Example of a Grafana dashboard:

![Grafana screenshot](https://github.com/coding-to-music/grafana-prometheus-node-js-example/blob/main/images/example-dashboard.png?raw=true)

## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/docker-statsd-influxdb-grafana.git
git push -u origin main
```

# Docker service with Telegraf (StatsD), InfluxDB and Grafana

:facepunch: Battle-tested

[![CircleCI](https://circleci.com/gh/samuelebistoletti/docker-statsd-influxdb-grafana.svg?style=svg)](https://circleci.com/gh/samuelebistoletti/docker-statsd-influxdb-grafana)

## Versions

### Warning: UPGRADE FROM OLDER VERSIONS TO VERSION 3.0.0 IS NOT POSSIBLE, SEE CHANGELOG.MD

* Main version:      3.0.0
* InfluxDB:          2.1.1
* Telegraf (StatsD): 1.21
* Postgres:          14.2.0
* Grafana:           8.4.4


## Quick Start

First download and install the latest available version of Docker Compose <https://docs.docker.com/compose/install/>

In order to start the service the first time launch:

```sh
COMPOSE_PROFILES=grafana,telegraf docker-compose up -d
```

You can replace `COMPOSE_PROFILES=grafana,telegraf` with the desired profiles to launch, you can launch only InfluxDB (default with no profiles).

To stop the service launch:

```sh
COMPOSE_PROFILES=grafana,telegraf docker-compose down
```

## Mapped Ports

```
Host		Container		Service

3000		3000			grafana
8086		8086		  	influxdb
8125		8125			statsd
```

## Grafana

Open <http://localhost:3000>

```
Username: admin
Password: admin
```

### Data source on Grafana

InfluxDB data source is automatically provisioned with new Flux language support flag.

## InfluxDB

### Web Interface

Open <http://localhost:8086>

```
Username: admin
Password: admin123456
Port: 8086
```

## Customizations

You can customize all settings in the attached config files, then you can stop and start the service in order to reload the new configurations.
