# microservices-proto

Definições protobuf e stubs Go gerados para os microsserviços do projeto de Programação Distribuída.

## Estrutura

```
microservices-proto/
├── order/
│   └── order.proto        # Definição das mensagens e serviço Order
└── golang/
    └── order/
        ├── order.pb.go       # Tipos gerados pelo protoc
        └── order_grpc.pb.go  # Server/client stubs gRPC gerados
```

## Serviços definidos

### Order
| RPC | Request | Response |
|-----|---------|----------|
| `Create` | `CreateOrderRequest` | `CreateOrderResponse` |

## Gerando o código Go

Instale o `protoc` e execute:

```bash
sh run.sh
```

O código gerado ficará em `golang/order/`.

## Dependências

- [protoc](https://grpc.io/docs/protoc-installation/) >= 25.x
- [protoc-gen-go](https://pkg.go.dev/google.golang.org/protobuf/cmd/protoc-gen-go)
- [protoc-gen-go-grpc](https://pkg.go.dev/google.golang.org/grpc/cmd/protoc-gen-go-grpc)
