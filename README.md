# multi-stage-builds-examples

## Before : NOT Use `multi-stage builds`

```sh
$ docker build -f Dockerfile.before -t kakakakakku/hello:before .

$ docker image ls kakakakakku/hello:before --format "table {{.Repository}}\t{{.Tag}}\t{{.Size}}"

REPOSITORY          TAG                 SIZE
kakakakakku/hello   before              327MB

$ docker run -it kakakakakku/hello:before
Hello, Go examples!
```

## After : Use `multi-stage builds`

```sh
$ docker build -f Dockerfile.after -t kakakakakku/hello:after .

$ docker image ls kakakakakku/hello:after --format "table {{.Repository}}\t{{.Tag}}\t{{.Size}}"
REPOSITORY          TAG                 SIZE
kakakakakku/hello   after               6.32MB

$ docker run -it kakakakakku/hello:after
Hello, Go examples!
```

## Documents

- [Use multi-stage builds | Docker Documentation](https://docs.docker.com/develop/develop-images/multistage-build/)
