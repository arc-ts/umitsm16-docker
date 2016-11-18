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