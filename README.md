<div align="center">
<img src="assets/helloworld-grpc-gateway.svg" width="400" />
<br />
<h1>Hello World gRPC-Gateway</h1>
<p>
Simple hello world program which uses gRPC-Gateway
</p>
<a href="https://github.com/iamrajiv/helloworld-grpc-gateway/network/members"><img src="https://img.shields.io/github/forks/iamrajiv/helloworld-grpc-gateway?color=0366d6&style=for-the-badge" /></a>
<a href="https://github.com/iamrajiv/helloworld-grpc-gateway/stargazers"><img src="https://img.shields.io/github/stars/iamrajiv/helloworld-grpc-gateway?color=0366d6&style=for-the-badge" /></a>
<a href="https://github.com/iamrajiv/helloworld-grpc-gateway/blob/master/LICENSE"><img src="https://img.shields.io/github/license/iamrajiv/helloworld-grpc-gateway?color=0366d6&style=for-the-badge" /></a>
</div>

## About Project

It is a simple hello world program which uses gRPC-Gateway. This project was created when I participated in Google Season of Docs with [gRPC-Gateway](https://github.com/grpc-ecosystem/grpc-gateway). The reason for making this project is to make people familiarize with gRPC-Gateway and how they can use gRPC-Gateway in their project.

I have added all tutorials related to it in [gRPC-Gateway documentation website](https://grpc-ecosystem.github.io/grpc-gateway/docs/tutorials/).

Folder structure:

```shell
.
├── LICENSE
├── Makefile
├── README.md
├── assets
│   └── helloworld-grpc-gateway.svg
├── buf.gen.yaml
├── buf.yaml
├── go.mod
├── go.sum
├── main.go
└── proto
    ├── google
    │   └── api
    │       ├── annotations.proto
    │       └── http.proto
    └── helloworld
        ├── hello_world.pb.go
        ├── hello_world.pb.gw.go
        ├── hello_world.proto
        └── hello_world_grpc.pb.go
```

## Usage

Before running this project install all the required Go packages by running the command `make install`. Also, you can generate the stubs using the command `make generate` and delete the stubs using the command `make clean`.

Start the server using the command:

```shell
$ go run main.go
```

Then use cURL to send HTTP requests:

```shell
$ curl -X POST -k http://localhost:8090/v1/example/echo -d '{"name": "hello"}'
```

```
{"message":"hello world"}
```

## License

[MIT](https://github.com/iamrajiv/helloworld-grpc-gateway/blob/master/LICENSE)
