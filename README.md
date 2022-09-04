# Way to Generate grpc.pb and pb for go

```
protoc -I ./proto \
  --go_out ./proto --go_opt paths=source_relative \
  --go-grpc_out ./proto --go-grpc_opt paths=source_relative \
  --grpc-gateway_out ./proto \
  --grpc-gateway_opt logtostderr=true \
  --grpc-gateway_opt paths=source_relative \
  --grpc-gateway_opt generate_unbound_methods=true \
  --openapiv2_out ./proto \
  --openapiv2_opt logtostderr=true \
  --openapiv2_opt use_go_templates=true \
  ./proto/hello/hello.proto
```
