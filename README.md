# Small JavaEE benchmark suite


## Goals

This small webapp is intended to give you a rough feeling about various different aspects of a JavaEE server installation.

Parts of it target the performance of the EE server implementation:
 * CDI 
 * EJB 
 * EL 
 * JSF

Other parts measure the performance of the underlying hardware:
 * large file disk IO
 * small file disk IO
 * cache memory throughput (small mem chunks)
 * RAM throughput (large mem chunks)

## Running

Just deploy the WAR and browse the page. It contains a download link to an Apache JMeter (http://jmeter.apache.org) benchmark script.

### Running locally on TomEE

$> mvn clean install tomee:run

Browse http://localhost:8080/eebench

### Running locally on Liberty Profile

__Prerequisite__:
 Download Liberty profile from [WASDev](https://developer.ibm.com/wasdev/downloads/) and store the file "wlp*.jar" locally.

#### Setup Liberty server
$> mvn liberty:create-server

####Run application
$> mvn clean install liberty:run-server

Browse http://localhost:9080/eebench

####Stop Liberty server
$> mvn liberty:stop-server


