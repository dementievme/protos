# Nutrition Protos for Backend

Contract descriptions for nutrition services.

How to install:
```
go get github.com/dementievme/nutrition-protos.git
```
How to generate code:
You need the ```protoc``` utility and the ```grpc``` plugin for golang.

1. Run Makefile for automatic code-generation start.
```
make proto
```
2. Run for manual code-generation start.
```
protoc -I proto proto/sso/v1/sso.proto --go_out=./gen/go --go_opt=paths=source_relative --go-grpc_out=./gen/go/ --go-grpc_opt=paths=source_relative
```