# hydra-jetty

This is a copy of jetty with the needed applications for running Hydra.  These include two java-based applications:

* [Fedora repository](http://fedora-commons.org/)
* [Solr](http://lucene.apache.org/solr/)

## Included Versions

* Jetty: 8.1.16
* Solr: 4.10.4
* Fedora: 3.7.0

## Usage

### Dependencies

* [Java 7 (JRE)](https://java.com/en/download/index.jsp)

### Manual

    git clone https://github.com/projecthydra/hydra-jetty
    cd hydra-jetty
    java -Xmx512m -jar start.jar

You can also change the port jetty starts on by editing the file etc/jetty.xml and changing this line to indicate a different port number:

    <Set name="port"><SystemProperty name="jetty.port" default="8983"/></Set>

### Using jettywrapper

For use within your Hydra application's Rails directory.

    rake jetty:install
    rake jetty:start

See [jettywrapper](https://github.com/projecthydra/jettywrapper) for more information regarding configuration and usage.
Port numbers and other java options maybe configured via the gem.

### Interaction

When jetty is finished initializing itself, Solr is available at

* [http://localhost:8983/solr/](http://localhost:8983/solr/)

and Fedora is available at

* [http://localhost:8983/fedora/](http://localhost:8983/fedora/)
* basic authorization is enabled an requires the username/password `fedoraAdmin/fedoraAdmin`

You can see a list of all installed applications at

* [http://localhost:8983](http://localhost:8983)
