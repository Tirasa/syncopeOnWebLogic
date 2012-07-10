Apache Syncope overlay to be run in Oracle WebLogic.
Practical implementation of official advices at Syncope [wiki](https://cwiki.apache.org/confluence/display/SYNCOPE/Run+Syncope+in+real+environments).

## How to test ##

This projects assumes that you have
 1. [Apache Maven 3.0](http://maven.apache.org) installed
 1. a running Oracle WebLogic instance, listening to port 7001
 1. a MySQL datasource named <code>syncopeDataSource</code> referring to an empty db

#### clone ####

<pre>
$ git clone git://github.com/ilgrosso/syncopeOnWebLogic.git
</pre>

#### build ####

<pre>
$ cd syncopeOnWebLogic
$ mvn clean package
</pre>

#### deploy ####

 1. <code>core/target/syncope.war</code>
 1. <console>console/target/syncope-console.war</code>

## Notes ##
 1. Currently on 1.0.0-incubating-SNAPSHOT, waiting for upcoming 1.0.0-incubating release.
 1. Not on 7001? Just put the correct listen port in <code>console/src/main/resources/configuration.properties</code>, re-build and re-deploy