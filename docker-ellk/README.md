Run the ELLK (Elasticseach, Logstash, Logspout, Kibana) stack with Docker and Docker-compose.

Based on the official images:

* [elasticsearch](https://registry.hub.docker.com/_/elasticsearch/)
* [logstash](https://registry.hub.docker.com/_/logstash/)
* [kibana](https://registry.hub.docker.com/_/kibana/)
* [logspout](https://registry.hub.docker.com/u/gliderlabs/logspout/)

# How to use it

Start using *docker-compose*:

```
$ docker-compose up
```

To run it in background (detached mode):

```
$ docker-compose up -d
```

### Playing with the stack

The stack exposes 3 ports on your localhost:

* 5000: Logstash UDP port
* 9200: Elasticsearch HTTP (with Marvel plugin accessible via [http://localhost:9200/_plugin/marvel](http://localhost:9200/_plugin/marvel))
* 5601: Kibana 4 web interface, access it via [http://localhost:5601](http://localhost:5601)


### Boot2docker

With *boot2docker*, you must access it via the *boot2docker* IP address:
* http://boot2docker-ip-address:9200/_plugin/marvel to access the Marvel plugin.
* http://boot2docker-ip-address:5601 to use Kibana 4.
