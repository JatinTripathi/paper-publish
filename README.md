# Paper Publish (Docker-Compose Binding)
A paper publishing web application constituting a self-explanatory Docker-Compose file.

Just clone this repository, cd into it and clone [API Gateway](https://github.com/JatinTripathi/api-gateway), [Editor Service](https://github.com/JatinTripathi/editor-service) and [Search Service](https://github.com/JatinTripathi/search-service) repositories in it.

Start Docker engine and type `docker-compose up` in terminal
This will build all the microservice images using there Dockerfile, and will download all the required official images from dockerhub.

There will be six containers, 
The first one will be API Gateway node.js container and its exposed port will be mapped on to the host's port no 8080 and this container will be linked to three containers:
* Mongodb container
* Search Service Container
* Editor Service Container

Then, Search service container will be linked to,
* Mongodb Container
* Search Service Container

And, Editor Service Container will be linked to,
* Elasticsearch Container
