# k.Node

Docker compose file to build a node of the infrastructure

## HOW TO

*The procedure is under revision*
To start, `docker` must be installed on the machine.
The infrastructure is installed as a docker service so we need a `docker swarm init` if a swarm is not present.

Change the `docker-compose.yaml` file to fit your needs.
Before starting, you need to register to the system the new node name and retrieve the node certificate.
To do it, please contact us at [support@ingetratedemodelling.org](mailto:support@ingetratedemodelling.org).

Then, change `node-name.yaml` to configure the application and substitute the file `application-node-name.cert` with the certificate.

Go to `docker-compose` folder and run the command below
```
docker stack deploy -c docker-compose.yaml projects-node --with-registry-auth
```
