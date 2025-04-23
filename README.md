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

Image can be prepared by using following command 
```
docker build .
docker build -t <tag for the image> .
```
