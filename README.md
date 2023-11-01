

## Prerequisites

- [Go](https://golang.org/) installed
- [Docker](https://www.docker.com/) installed (if Docker is used)

## Without Docker
git clone https://github.com/ayush-sri323/User.git
cd User
go build -o main
go run ./main

cd user_client
go run user_client.go

## With Docker

1. Clone the repository with these command:
git clone https://github.com/ayush-sri323/User.git
cd User

docker build -t grpc-service-server -f Dockerfile.server .
docker run -p 50051:50051 --network mynetwork grpc-service-server
docker build -t grpc-service-client -f Dockerfile.client .
docker run --network mynetwork grpc-service-client


