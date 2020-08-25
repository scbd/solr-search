

 docker run -p 8984:8983 -v "$PWD/solrdata:/var/solr" scbd/solr:8.5.2-test solr-precreate scbdTest /opt/solr/server/solr/configsets/scbdConf
 docker run -p 8984:8983 -v "$PWD/solrdata/solr/data:/var/solr/data"  scbd/solr:8.5.2-test solr-precreate scbdTest /opt/solr/server/solr/configsets/scbdConf

#   -v "$PWD/solrdata/solr/backups:/opt/solr/custom-backups"

 curl http://localhost:8983/solr/scbd/config -H 'Content-type:application/json' -d'{ "set-property" : {"requestDispatcher.requestParsers.enableStreamBody":true} }'

 curl -H 'Content-type:application/json' -d '{"set-property": {"requestDispatcher.requestParsers.enableStreamBody": true}}' http://localhost:8983/solr/scbd/config