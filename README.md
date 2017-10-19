# spring-cloud-config-server-local

mvn clean -Dmaven.test.skip docker:build
docker run -p 10010:10010 -t spring-cloud/config-server-local
