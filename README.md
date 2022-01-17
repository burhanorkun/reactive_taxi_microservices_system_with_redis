# Taxi System Microservices with Spring boot, Redis, Nginx, Reactive

$ mvn clean install

$ docker-compose build

$ docker-compose up -d or $ docker-compose up --scale taxi-service-app=2 -d
(docker-compose up --scale <APP_NAME>=2 -d)

$ docker-compose down

### Create new taxi (POST)

http://localhost/taxis

```json
{
  "taxiType": "NANO"
}
```

### Update location (PUT)

http://localhost/taxis/9383a90c-8d7e-4444-8bf8-544e003f7b03/location

```json
{
  "latitude": 6.938020,
  "longitude": 79.963855
}
```

### Update taxi status (PUT)

http://localhost/taxis/9383a90c-8d7e-4444-8bf8-544e003f7b03/status?status=OCCUPIED

### Get available taxi (GET)

http://localhost/taxis/9383a90c-8d7e-4444-8bf8-544e003f7b03/status

