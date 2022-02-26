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
$ docker-compose -f docker-compose.yml up -d
```

OpenSearch and Dashboards (localhost:5601):

```
$ docker-compose -f docker-compose.yml -f docker-compose.dashboards.yml up -d
```

OpenSearch cluster:

```
$ docker-compose -f docker-compose.yml -f docker-compose.cluster.yml up -d
```

OpenSearch cluster and Dashboards:

```
$ docker-compose -f docker-compose.yml -f docker-compose.cluster.yml -f docker-compose.dashboards.yml up -d
```

### Stop Fess

```
$ docker-compose -f docker-compose.yml -f ...(snip)... down

```

### Remove Local Volumes

```
$ docker volume rm docker-opensearch_opensearch-data1 docker-opensearch_opensearch-data2

```
