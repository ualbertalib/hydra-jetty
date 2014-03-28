HYDRA-JETTY
--------------------------
This is a copy of jetty pre-installed with various applications needed by Hydra 
applications.
Most notably, these include Fedora 4 alpha 4 (https://github.com/futures/fcrepo4/releases/tag/fcrepo-4.0.0-alpha-4) and 
solr (http://lucene.apache.org/solr/).  

To run, use 

  java -jar start.jar

When jetty is finished initializing itself, Solr is available at 

  	http://localhost:8983/solr/development/admin/
  	http://localhost:8983/solr/test/admin/

and fedora is available at 

	http://localhost:8983/fedora/

You can see a list of all installed applications at http://localhost:8983

You can also change the port jetty starts on by editing the file etc/jetty.xml 
and changing this line to indicate a different port number:

<Set name="port"><SystemProperty name="jetty.port" default="8983"/></Set>


Included Versions
-----------------
jetty: 8.1.8.v20121106
solr: 4.3.0
fedora: 4.0.0a4 
