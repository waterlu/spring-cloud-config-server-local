# spring-cloud-config-server-local

mvn clean package -Dmaven.test.skip docker:build
docker run --name config-server -d -p 10010:10010 spring-cloud/config-server-local
docker logs -f config-server


docker rm $(docker ps -qf status=exited)
docker rmi $(docker images -q -f dangling=true)
docker start
docker stop