# RabbitMQ Go

A collection of Go programs for interacting with RabbitMQ.

## Pre-Req

- Install Docker
- Install GoLang
- Install Go package dependencies

## Install Go Packages

The command below will install the Go package `amqp`.
```sh
$ go get github.com/streadway/amqp
```

## Running the application

1. Start the RabbitMQ docker container by running the `runDocker.sh` script in one terminal:
   ```sh
   $ ./runDocker.sh
   ```
2. In another terminal run the `receive.go` Go program:
   ```sh
   $ go run receive.go
   ```
3. In another terminal run the `send.go` Go program to send a message to the RabbitMQ message broker:
   ```sh
   $ go run send.go
   ```

## What this does

The commands above will:
1. create a RabbitMQ Docker service,
2. connect to the RabbitMQ channel and wait for messages,
3. send a message to a channel in RabbitMQ,
4. and print out the message received from RabbitMQ.

## Teardown the Docker service

To stop and tear down the RabbitMQ Docker service, simply run:
```sh
$ ./downDocker.sh
```