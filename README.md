# SpringCloudEurekaConfigServer

Config server url :

http://localhost:8888/employee-producer/employee-producer.properties

Eureka Server URL : 

http://localhost:8090/


# spring-cloud-configserver-Git

Basic example of using spring-cloud-config to retrieve configs from local disk space.


## Quick Start

Build code
git clone https://github.com/krishna8485/SpringCloudConfigServerLocalRef.git
cd SpringCloudConfigServerLocalRef

### Start Config Server

cd employee-config-server
gradle clean bootrun
Load http://localhost:8888. This displays the config properties which are being retrieved from the git repo defined in application.properties. This currently is the config directory in this repository.

### Start Eureka Server

cd EurekaServer
gradle clean bootrun
Load http://localhost:8090 to register the services.

### Start Employee-producer

gradle clean bootrun
Load http://localhost:8081/employee displays the employee response. Reads the eureka register url from properties in config server and register to eureka during startup.


curl -X POST 'http://localhost:8081/employee'


