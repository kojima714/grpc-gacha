# GRPC for gacha 

This is minimum microservice for GRPC with gacha architecture.

1. Client sends some cards data
2. Server receive cards and response lottery one
3. Client get a card and output card name

## Requirement

### use only

- grpc
- Protocol Buffer 3
- Ruby
    - Ruby 2 or higher
- Golang
    - Go 1.5 or higher

### build proto file

- Ruby
    - grpc-tools (install with gem)
- Golang
    - proto-gen-go

### how to generate grpc code

- Ruby
    - grpc_tools_ruby_protoc -I proto --ruby_out=lib --grpc_out=lib proto/gacha.proto
- Golang
    - protoc -I proto --go_out=plugins=grpc:lib/gacha proto/gacha.proto
