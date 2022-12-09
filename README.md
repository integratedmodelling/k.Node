# k.Node

Docker compose file to build a node infrastructure

## HOW TO

*The procedure id under revision*
To start, `docker` must be installed on the machine.
The infrastructure is mounted as a docker service so we need a `docker swarm init` if a swarm is not present.

Change the `docker-compose.yaml` file to fit your needs.
Before start, you need to regiter in the system the new node name and retrieve the node certificate.
To do it, please contact us using [support@ingetratedemodelling.org](mailto:support@ingetratedemodelling.org).

After it, change `node-name.yaml` to config the application and substitute the file `application-node-name.cert` with the certificate.

Go to `docker-compose` folder and run
```
docker stack deploy -c docker-compose.yaml projects-node --with-registry-auth
```