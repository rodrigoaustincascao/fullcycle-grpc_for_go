## Instalando compilador e plugins
```
<!-- Instalar o compilador -->
$ apt install -y protobuf-compiler
$ protoc --version  # Ensure compiler version is 3+


<!-- Gera as entidades/mensagens -->
$ go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28

<!--Gera todas as interfaces de comunicação  -->
$ go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2
```

## Iniciar o projeto
```
go mod init <NomeProjeto>

go mod tidy
```
## Client GRPC
https://github.com/ktr0731/evans

### Gerar as entidades
Gerar os arquivos e as interfaces 
```
protoc --go_out=. --go-grpc_out=. proto/course_category.proto
```

### Executar o EVANS
```
# Se o seu servidor estiver habilitando a reflexão gRPC , você poderá iniciar o Evans apenas com a opção -r( --reflection).

$ evans -r repel
# ou 
evans --proto course_category.proto

# selecionando o service
service <NomeService>

# sair do evans
Ctrl + D
```
### Executar uma chamada para o Evans
```
call <Nome>


```


# SQL
```
sqlite3 db.sqlite

create table categories(id string, name string, description string);
```