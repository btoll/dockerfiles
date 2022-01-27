# tor-browser Dockerfile

This is Jessie Frazelle's [`tor-browser` Dockerfile](https://github.com/jessfraz/dockerfiles/tree/master/tor-browser).

## Create a container

```
xhost +local:root
docker container rm tor-browser
docker run --device /dev/snd -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/shm:/dev/shm -v /etc/machine-id:/etc/machine-id:ro -e DISPLAY=unix:0 -e TOR_VERSION=10.5.6 --name tor-browser jessfraz/tor-browser:latest &> /dev/null &
```

# References

- [jessfraz/tor-browser on Docker Hub](https://hub.docker.com/r/jessfraz/tor-browser)
- [Jessie Frazelle's Blog](https://blog.jessfraz.com/)

