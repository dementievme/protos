PROTOC := protoc

.PHONY: proto

proto:
	@echo "Generating Go code from proto..."
	@command -v $(PROTOC) >/dev/null || (echo "protoc not found"; exit 1)
	@command -v protoc-gen-go >/dev/null || (echo "install protoc-gen-go"; exit 1)
	@command -v protoc-gen-go-grpc >/dev/null || (echo "install protoc-gen-go-grpc"; exit 1)

	protoc -I proto proto/sso/v1/sso.proto \
		--go_out=./gen/go --go_opt=paths=source_relative \
		--go-grpc_out=./gen/go --go-grpc_opt=paths=source_relative
