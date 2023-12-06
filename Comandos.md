## Comandos de docker compose para ejecutar las distintas infraestructuras

docker-compose -f dan-mysql.yml -p mysql-infra up --build -d
docker-compose -f dan-mongo.yml -p mongo-infra up --build -d
docker-compose -f dan-pg.yml -p pg-infra up --build -d
docker-compose -f dan-ms.yml -p ms-infra up --build -d


docker-compose -f dan-mysql.yml -f dan-mongo.yml -f dan-pg.yml -f dan-ms.yml -f dan-cloud.yml -f dan-telemetria.yml -p dan-tp-infra up --build -d



docker-compose  -p mongo-infra up --build -d
docker-compose -p pg-infra up --build -d
docker-compose  -p ms-infra up --build -d

buildear la infra de mysql
```
docker-compose -f dan-mysql.yml -p mysql-infra up --build -d
```

buildear la infra de postgres
```
docker-compose -f dan-pg.yml -p pg-infra up --build -d
```

buildear la infra de mongo
```
docker-compose -f dan-mongo.yml -p mongo-infra up --build -d
```

docker run -d --hostname my-rabbit -p5672:5672 --name some-rabbit rabbitmq:3
docker run -d --hostname my-rabbit -p5672:5672 -p15672:15672 --name some-rabbit -e RABBITMQ_DEFAULT_USER=dan -e RABBITMQ_DEFAULT_PASS=password rabbitmq:3-management


docker-compose -f dan-tp.yml -p dan-tp up --build -d
