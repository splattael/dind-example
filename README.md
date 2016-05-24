# Docker in docker (dind) example

Just run:

```
docker-compose up
```

## What happened?

Docker compose starts a docker engine inside a docker (dind).

Other services (`node1`, `node2`) can use this docker engine in isolation
by setting the environment variable `DOCKER_HOST` pointing to linked
(and *insecure* -> port 2375) docker service `docker-in-docker`.

Note that the output of each node shows nothing which means that the linked
docker engine is actually running in isolation.
