This project shows a Camel Route using an AMQ broker. For an example running the same camel route in OpenShift and using an AMQ broker, see  [Karaf2-camel-amq](https://github.com/gbengataylor/karaf2-camel-amq)

This project assumes a broker is running on localhost:61616. This can be modified

To build this project use

    mvn install

To run this project

    mvn camel:run

To run this project on JBoss Fuse shell :

    -  create a properties file named camel.activemq.spring.conf in etc folder of JBoss Fuse containing ActiveMQ
      connection options, i.e :

      broker.url       = tcp://localhost:61616
      broker.username  = admin
      broker.password  = admin
      
    - install dependencies from Fuse shell:
	
	  features:install activemq-camel

    - install the bundle from Fuse shell

      install -s mvn:com.mycompany/camel-activemq-blueprint/1.0.0-SNAPSHOT

