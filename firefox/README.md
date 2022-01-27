# tor-browser Dockerfile

This is Jessie Frazelle's [`firefox` Dockerfile](https://github.com/jessfraz/dockerfiles/tree/master/firefox).

## Create a container

```
xhost +local:root
docker container rm firefox
docker run --device /dev/snd -v /tmp/.X11-unix:/tmp/.X11-unix -v /dev/shm:/dev/shm -v /etc/machine-id:/etc/machine-id:ro -e DISPLAY=unix:0 --name firefox jessfraz/firefox:latest  &> /dev/null &
```

# References

- [jessfraz/firefox on Docker Hub](https://hub.docker.com/r/jessfraz/firefox)
- [Jessie Frazelle's Blog](https://blog.jessfraz.com/)

