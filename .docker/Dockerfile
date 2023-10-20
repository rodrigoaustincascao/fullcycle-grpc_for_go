FROM mcr.microsoft.com/devcontainers/go:1-1.21-bullseye

WORKDIR /go/src

RUN apt update \
  && apt install -y protobuf-compiler

RUN go install google.golang.org/protobuf/cmd/protoc-gen-go@v1.28
RUN go install google.golang.org/grpc/cmd/protoc-gen-go-grpc@v1.2  
RUN go install github.com/ktr0731/evans@latest

# Add write permission for /go/pkg
RUN chmod -R a+w /go/pkg

USER vscode


ENTRYPOINT ["tail", "-f", "/dev/null"]