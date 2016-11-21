# docker-nodejs

* build.sh: build docker image.

```
docker build -t nodejs ./src
```

* start.sh: start daemon container instance.

```
docker run --name=nodejs -d --restart always nodejs
```

* stop.sh: stop and remove container instance.

```
docker stop nodejs; docker rm nodejs
```

* log.sh: show container log from standard output.

```
docker logs nodejs
```
