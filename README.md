# conversao-distancia

## running the application

### with docker (only)
```
docker build -t conversao-distancia-app .
docker run -it --rm --name my-running-app conversao-distancia-app
docker exec -it my-running-app curl -vvv http://localhost:5000
docker exec -it my-running-app curl -X POST --data-raw 'selectTemp=1&valorRef=123' -vvv http://localhost:5000
```

### with docker compose
```
docker compose up
docker compose exec app curl -vvv http://localhost:5000
docker compose exec app curl -X POST --data-raw 'selectTemp=1&valorRef=123' -vvv http://localhost:5000
```