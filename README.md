# Go Web Application

This is a simple website written in Golang. It uses the `net/http` package to serve HTTP requests.

## Build app

```bash
go build -o main .
```

## Running the server

To run the server, execute the following command:

```bash
go run main.go
```

The server will start on port 8080. You can access it by navigating to `http://localhost:8080/courses` in your web browser.

## Looks like this

![Website](static/images/golang-website.png)

# Docker Commands

## Build container

```sh
docker build -t go-app:v1.0.0 .
```

```sh
docker run -d -p 8080:8080 --name go-app go-app:v1.0.0
```

## Push Container

```sh
aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 395691671709.dkr.ecr.us-east-1.amazonaws.com
```

```sh
docker tag go-app:v1.0.0 395691671709.dkr.ecr.us-east-1.amazonaws.com/go-app:v1.0.0
docker push 395691671709.dkr.ecr.us-east-1.amazonaws.com/go-app:v1.0.0
```