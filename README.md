# Local

## How-tos

### Spin up environment

In Iterm2:

* `docker-machine start default`
* `docker-machine env`
* `eval $(docker-machine env)`

From project root:

* `docker login`
* `docker-compose up`

### Local alias

Add local.dev to your /etc/hosts file. IP is probably 192.168.99.100 but you can double check with
`docker-machine ip default`.

### Access shell in a container
 
 `docker exec -it local_web_1 bash`

