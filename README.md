# Docker Engine

Docker engine is an open source technology for building and containerizing applications. Docker engine acts as client-server application.

- Server with long running daemon process _dockerd_.
- API which specify interface that programs can  use to talk and instruct docker daemon.
- Command line interface client _docker_.

CLI uses _Docker API_ to control or interact with _Docker daemon_ through scripting or CLI Commands.

#### Docker Objects
- Image
- Containers
- Services
- Networks
- Volumes

##### Images  

These are read-only templates used to create containers. They contain neccessary information to run containers.

There are two important principles of images:

- Images are immutable. Once an image is created, it can't be modified. You can only make a new image or add changes on top of it.
- Container images are composed of layers. Each layer represents a set of file system changes that add, remove, or modify files.

Docker images can be found at DockerHub (https://hub.docker.com/) or Microsoft Public repo (https://mcr.microsoft.com/) which is common public repository or any private repositories.

Images can be created using _Dockerfile_ and can be pushed to public or private repositories.

Image can be created by using following command 
```
docker build .
docker build -t <tag for the image> .
```
In above command Docker Build implements a client-server architecture, where:

- Client: Buildx is the client and the user interface for running and managing builds.
- Server: BuildKit is the server, or builder, that handles the build execution.

When you invoke a build, the Buildx client sends a build request to the BuildKit backend. BuildKit resolves the build instructions and executes the build steps. The build output is either sent back to the client or uploaded to a registry, such as Docker Hub.

Buildx and BuildKit are both installed with Docker Desktop and Docker Engine out-of-the-box. When you invoke the docker build command, you're using Buildx to run a build using the default BuildKit bundled with Docker.
