1. Setup the ElasticSearch data directory:

```
$ chmod -R g+rwx elasticsearch/data
$ chown -R 1000:1000 elasticsearch/data
```

2. Increase the virtual memory map limit:

```
# sysctl -w vm.max_map_count=262144
```

3. Start the environment:

```
$ docker-compose up
```

4. Check the ElasticSearch cluster health:

```
$ curl -X GET "localhost:9200/_cluster/stats?human&pretty" | jq .
```

5. Access Kibana at http://localhost:5601

