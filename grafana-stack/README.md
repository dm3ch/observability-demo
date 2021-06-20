# Grafana observability stack demo
This demo is based on https://github.com/grafana/tns/tree/main/production/docker-compose

## How to run
This demo using docker-compose to bring up a complete stack with the demo app, including Grafana, Prometheus, Loki and Tempo.
The datasources and cross-datasource links should all be configured correctly.

To run:

```shell
$ docker plugin install grafana/loki-docker-driver:latest --alias loki --grant-all-permissions
$ docker-compose up -d
```

The navigate to http://localhost:3000 to see Grafana.

If you have any problems, run `docker-compose up -d` first.

## Overview of correlation features
During the test I was able to view/filter all types of observability data - logs/traces/metrics.
But I wasn't able to use all correlation features, maybe they would be available after better configuration.

But you can find description of that features there - https://grafana.com/blog/2020/03/31/how-to-successfully-correlate-metrics-logs-and-traces-in-grafana/
