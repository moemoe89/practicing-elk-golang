[![CircleCI](https://circleci.com/gh/moemoe89/go-elk-hiro.svg?style=svg)](https://circleci.com/gh/moemoe89/go-elk-hiro)
[![codecov](https://codecov.io/gh/moemoe89/go-elk-hiro/branch/master/graph/badge.svg)](https://codecov.io/gh/moemoe89/go-elk-hiro)
[![Go Report Card](https://goreportcard.com/badge/github.com/moemoe89/go-elk-hiro)](https://goreportcard.com/report/github.com/moemoe89/go-elk-hiro)

# GO-ELK-HIRO #

Practicing ELK Stack Using Golang (Echo Framework) as Programming Language, ELK (Elasticsearch Logstash Kibana) as Service

## Directory structure
Your project directory structure should look like this
```
  + your_gopath/
  |
  +--+ src/github.com/moemoe89
  |  |
  |  +--+ go-elk-hiro/
  |     |
  |     +--+ main.go
  |        + api/
  |        + routers/
  |        + ... any other source code
  |
  +--+ bin/
  |  |
  |  +-- ... executable file
  |
  +--+ pkg/
     |
     +-- ... all dependency_library required

```

## Setup and Build

* Setup Golang <https://golang.org/>
* Setup ELK Stack <https://www.elastic.co/>
* Under `$GOPATH`, do the following command :
```
$ mkdir -p src/github.com/moemoe89
$ cd src/github.com/moemoe89
$ git clone <url>
$ mv <cloned directory> go-elk-hiro
```

## Running Application
Make config file for local :
```
$ cp config-sample.json config.json
```
Build
```
$ go build
```
Run
```
$ go run main.go
```

## How to Run with Docker
Make config file for docker :
```
$ cp config-sample.json config.json
```
Build
```
$ docker-compose build
```
Run
```
$ docker-compose up
```
Stop
```
$ docker-compose down
```

## How to Test the Log
Make some log by hit the endpoints :
```
$ curl localhost:8788/error
$ curl localhost:8788/info
$ curl localhost:8788/warn
```
Navigate kibana on your browser :
```
localhost:5601
```
