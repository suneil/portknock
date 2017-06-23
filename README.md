# portknock

Just an simple litte utility I developed to test port accessibility
within docker containers as most of them don't have any utilities like nmap or telnet

To compile for Linux on Intel platforms
```bash
GOOS=linux GOARCH=amd64 go build
```

And then copy into docker container

```bash
docker cp portknock mycontainer:/tmp/portknock
```

Shell into the container and execute

```bash
docker exec -it CONTAINER_ID /bin/bash
/tmp/portknock poke hostname port
```