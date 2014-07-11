Running docker on an external server
------------------------------------

Add the following to the remote docker server init script
```
-H 0.0.0.0:4243
```
Then add the following to your local machine where you want to run the docker commands
```bash
export DOCKER_HOST=tcp://host.of.your.server.net:4243
```
Make sure you add any needed firewall rules to allow 4243

The real downside is that the client and the server need to be the same version or Docker will complain