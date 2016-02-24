## ![Spring Framework](../images/spring-framework.png)
# Spring Framework
## Far beyond CDI

---

# A bit of history
![Spring Framework](../images/spring-timeline.png)

---

## Expert One-on-One J2EE Development without EJB
* Architectural principles on how to solve core problems:
  * Transaction management, persistence, remoting, and Web tier design
* Leveraging practical techniques and tools in order to create a lightweight architecture;

---

### Version 1.0
* ***AOP interception*** framework based on the AOP Alliance interfaces, integrated with the core container
* ***JNDI support classes***, allowing for easy wiring of Spring-managed beans with JNDI-located objects
* ***Application context concept***, providing resource loading and message access abstractions
* ***Generic transaction management*** with pluggable strategies, supporting declarative and programmatic demarcation
* Support for ***source-level metadata***, with Commons Attributes as default implementation (e.g. for transaction attributes)

--

* ***Generic DAO support***, providing a generic data access exception hierarchy for use with any data access strategy
* ***JDBC abstraction*** that simplifies resource and error handling, also covering BLOB/CLOB support
* ***Hibernate support***, providing SessionFactory management and transaction-scoped ThreadLocal Sessions
* Support classes for ***JDO 1.0 and iBATIS*** SQL Maps 1.3/2.0, integrated with Spring’s transaction management
* ***Mail sender abstraction***, with special support for JavaMail including convenient handling of file attachments

--

* ***Scheduling support for Quartz and Timer***, making it easy to invoke methods of Spring-managed beans
* ***Remoting support for RMI, JAX-RPC*** and Caucho’s Hessian/Burlap, for easy exposure of Spring-managed beans
* Convenience classes for ***accessing and implementing EJBs***, both local and remote
* ***Web application context***, for loading a Spring application context in a web environment
* ***Flexible web MVC framework***, built on strategy interfaces and integrated with various view technologies
* https://spring.io/blog/2004/03/24/spring-framework-1-0-final-released

---

### Pivotal = SpringSource + Vmware + EMC + GE

* Interface 21 - Rod Johnson
* SpringSource + Covalent = $$$
* SpringSource + G2One = Flexibility
* SpringSource + Hyperic = Gets to the cloud
* SpringSource + Cloud Foundry = PaaS ready
* Now SpringSource is inside the: Apache Tomcat, Apache HTTP Server, Hyperic, Groovy, and Grails  Java Community Process communities

--

* August 2009 VMware buys SpringCloud for $ 420M
* And create the vFabric Application Suite
  * Among the vFabric products acquire:
    * RabbitMQ
    * Redis
    * GemStone
* Then Pivotal rises as a joint venture

---

### Version 4.0
* Java 8 (as well as 6 and 7)
  * Lambda expressions and method references with Spring’s callback interfaces
  * There is first-class support for java.time (JSR-310)
  * Several existing annotations have been retrofitted as @Repeatable
  * Java 8’s parameter name discovery (based on the -parameters compiler flag) as an alternative to compiling your code with debug information enabled.
  * Remains compatible with older versions of Java and the JDK

--

* Java EE
  * JPA 2.0 and Servlet 3.0
* Supports the Java EE 7 level of applicable specifications:
  * JMS 2.0
  * JTA 1.2
  * JPA 2.1
  * Bean Validation 1.1
  * JSR-236 Concurrency Utilities

--

* Groovy Bean Definition DSL as XML replacement
```groovy
def reader = new GroovyBeanDefinitionReader(myApplicationContext)
reader.beans {
    dataSource(BasicDataSource) {
        driverClassName = "org.hsqldb.jdbcDriver"
        url = "jdbc:hsqldb:mem:grailsDB"
        username = "sa"
        password = ""
        settings = [mynew:"setting"]
    }
    sessionFactory(SessionFactory) {
        dataSource = dataSource
    }
    myService(MyService) {
        nestedBean = { AnotherBean bean ->
            dataSource = dataSource
        }
    }
}
```

--

* Core Container Improvements:
* General Web Improvements
* WebSocket, SockJS, and STOMP Messaging
* Testing Improvements

---

![Spring Framework](../images/spring-overview.png)

Note:
http://docs.spring.io/spring-framework/docs/current/spring-framework-reference/html/overview.html#overview-modules

--

### Artifacts

* spring-aop - ***Proxy-based AOP support***
* spring-aspects - ***AspectJ based aspects***
* spring-beans - ***Beans support, including Groovy***
* spring-context - ***Application context runtime, including scheduling and remoting abstractions***
* spring-context-support - ***Support classes for integrating common third-party libraries into a Spring application context***
* spring-core - ***Core utilities, used by many other Spring modules***
* spring-expression - ***Spring Expression Language (SpEL)***

--

* spring-instrument - ***Instrumentation agent for JVM bootstrapping***
* spring-instrument-tomcat - ***Instrumentation agent for Tomcat***
* spring-jdbc - ***JDBC support package, including DataSource setup and JDBC access support***
* spring-jms - ***JMS support package, including helper classes to send and receive JMS messages***
* spring-messaging - ***Support for messaging architectures and protocols***
* spring-orm - ***Object/Relational Mapping, including JPA and Hibernate support***
* spring-oxm - ***Object/XML Mapping***

--

* spring-test - ***Support for unit testing and integration testing Spring components***
* spring-tx - ***Transaction infrastructure, including DAO support and JCA integration***
* spring-web - ***Web support packages, including client and web remoting***
* spring-webmvc - ***REST Web Services and model-view-controller implementation for web applications***
* spring-webmvc-portlet - ***MVC implementation to be used in a Portlet environment***
* spring-websocket - ***WebSocket and SockJS implementations, including STOMP support***

---

#![Spring Framework](../images/spring-projects.png)

--

* ***Spring IO Platform*** - Provides a cohesive, versioned platform for building modern applications. It is a modular, enterprise-grade distribution that delivers a curated set of dependencies
* ***Spring Boot*** - Takes an opinionated view of building Spring applications and gets you up and running as quickly as possible
* ***Spring Cloud*** - Spring Cloud provides tools for developers to quickly build some of the common patterns in distributed systems

--

* ***Spring Data*** - JPA, Mongo, Neo4J, Redis, SOLR, Hadoop, Gemfire, JDBC, Couchbase, ElasticSearch, Cassandra, Dynamo
* ***Spring Integration*** - Extends the Spring programming model to support the well-known Enterprise Integration Patterns
* ***Spring Batch*** - A lightweight, comprehensive batch framework designed to enable the development of robust batch applications vital for the daily operations of enterprise systems

--

* ***Spring Social*** - Facebook, Twitter, Linkedin & extensible core
* ***Spring Session*** - API session, Http Session, Websocket, Cluster, Multi browser...
* ***Spring Android*** - Android REST Client, Support for secure APIs, Social Integration

--

### Spring XD

The project's goal is to simplify the development of big data applications.

![Spring XD](../images/spring-xd-unified-platform-for-big-data.png)

---

#Lets have some fun...

---

### Links
http://www.infoworld.com/article/2925047/application-development/build-self-healing-distributed-systems-with-spring-cloud.html

https://github.com/joshlong

http://spring.io/projects

http://start.spring.io

---

### Thanks for the audience
[@_oliveira_tiago](https://twitter.com/_oliveira_tiago)

[https://github.com/tiagodeoliveira](https://github.com/tiagodeoliveira)

[tiagodeoliveira.github.io](tiagodeoliveira.github.io)
