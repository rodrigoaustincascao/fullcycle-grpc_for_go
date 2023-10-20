# Instalando compilador e plugins
```
<!-- Instalar o compilador -->
$ apt install -y protobuf-compiler
$ protoc --version  # Ensure compiler version is 3+


<!-- Gera as entidades/mensagens -->
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28

<!--Gera todas as interfaces de comunicação  -->
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```

# Iniciar o projeto
```
go mod init <NomeProjeto>

go mod tidy
```

# Gerar as entidades
Gerar os arquivos e as interfaces 
```
protoc --go_out=. --go-grpc_out=. proto/course_category.proto
```

# Client GRPC
https://github.com/ktr0731/evans