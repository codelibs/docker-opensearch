Docker Compose for OpenSearch
=======================

## Description

This is an example compose file for running OpenSearch with Docker Compose.

### Kernel settings for elasticsearch

OpenSearch needs to set `vm.max_map_count` to at least 262144. See [Important settings](https://opensearch.org/docs/latest/opensearch/install/important-settings).

## Usage

### Run OpenSearch

OpenSearch for single node (localhost:9200):

```
$ docker compose -f compose.yaml up -d
```

OpenSearch and Dashboards (localhost:5601):

```
$ docker compose -f compose.yaml -f compose-dashboards.yaml up -d
```

OpenSearch cluster:

```
$ docker compose -f compose.yaml -f compose-cluster.yaml up -d
```

OpenSearch cluster and Dashboards:

```
$ docker compose -f compose.yaml -f compose-cluster.yaml -f compose-dashboards.yaml up -d
```

### Stop Fess

```
$ docker compose -f compose.yaml -f ...(snip)... down

```

### Remove Local Volumes

```
$ docker volume rm docker-opensearch_opensearch-data1 docker-opensearch_opensearch-data2

```
