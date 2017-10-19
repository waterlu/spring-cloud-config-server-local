# spring-cloud-config-server-local

mvn clean package -Dmaven.test.skip docker:build
docker run -p 10010:10010 -t spring-cloud/config-server-local --name config-server
docker logs -f config-server