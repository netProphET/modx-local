# Local

## How-tos

### Spin up environment

If you're using Docker Machine, run these commands:

* `docker-machine start default`
* `docker-machine env`
* `eval $(docker-machine env)`

From project root:

* `docker login`
* `docker-compose up`

### Local alias

Add local.dev to your /etc/hosts file. IP is probably 192.168.99.100 but you can double check with
`docker-machine ip default`.

Then you access things in the project's `www` folder like this:

`www/modx-123` => `http://local.dev/modx-123/`

### Access shell in one of the containers
 
 `docker exec -it local_web_1 bash`

(or `local_db_1` etc)

### General Use

You can throw multiple revo installs in the `www` directory. Just note they'll be operating in a subdirectory, URL-wise.

PHPStorm makes it pretty easy to get the debugger going from inside the containers. Multiple tutorials around the web for that.
