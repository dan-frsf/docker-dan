## Comandos de docker compose para ejecutar las distintas infraestructuras

buildear la infra de mysql
```
docker-compose -f dan-mysql.yml -p mysql-infra up --build -d
```

buildear la infra de postgres
```
docker-compose -f dan-pg.yml -p pg-infra up --build -d
```