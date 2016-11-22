## Demo 1 - helloworld
```
docker build -t helloworld demo1-helloworld/
docker run helloworld
```


## Demo 2 - layers
```
docker build -t layers demo2-layers/
docker run layers
docker history layers
```

## Demo 3 - from
```
docker build -t from demo3-from/
docker run from
docker history from
```

## Demo 4 - Run
* visit http://localhost:8888 when up

```
docker pull nginx:stable-alpine
```

**unix/linux**
```
docker run -d -v $(pwd)/demo4-run:/usr/share/nginx/html -p 8888:80 nginx:stable-alpine
```

**windows**
```
docker run -d -v %cd%/demo4-run:/usr/share/nginx/html -p 8888:80 nginx:stable-alpine
```

## Compose

* Requires installing compose for your system: https://docs.docker.com/compose/install/
* Visit http://localhost when up

```
docker-compose -f compose-wordpress/docker-compose.yml up -d
```

**To clean up**
```
docker-compose -f compose-wordpress/docker-compose.yml stop
docker-compose -f compose-wordpress/docker-compose.yml rm -f
docker volume rm composewordpress_db_data
docker network rm backend
docker network rm public
```
