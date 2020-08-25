Solr can have many collections/cores and they all need to live somewhere.

Solr home is that location and is marked by the presence of solr.xml file.

Then, when Solr server is started, it can be pointed to the right directory with -s option:
bin/solr start -s <path-to-solr.xml-dir>
