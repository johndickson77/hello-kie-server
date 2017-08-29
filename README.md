# Hello Kie Server
First steps with Kie Server 6.3. For more information see [this article](http://www.mastertheboss.com/jboss-jbpm/jbpm6/running-rules-on-wildfly-with-kie-server) on master the boss.

Kie Server Access: http://localhost:8080/kie-server-6.5.0.Final-ee7/services/rest/server

Create Container: curl -X PUT -H Content-type:application/xml -u kieserver:password1! --data @createHelloContainer.xml http://localhost:8080/kie-server-6.5.0.Final-ee7/services/rest/server/containers/hello

Create Scanner: curl -X PUT -H Content-type:application/xml -u kieserver:password1! --data @createHelloScanner.xml http://localhost:8080/kie-server-6.5.0.Final-ee7/services/rest/server/containers/hello/scanner

Test Container: curl -u kieserver:password1! -H Accept:application/json http://localhost:8080/kie-server-6.5.0.Final-ee7/services/rest/server/containers/hello

Test Request: curl -X POST -H X-KIE-ContentType:JSON -H Content-type:application/json -u kieserver:password1! --data @droolsCommands.json http://localhost:8080/kie-server-6.5.0.Final-ee7/services/rest/server/containers/instances/hello