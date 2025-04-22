# Packages in Golang
Part of Workshop "Basics of Go" from Frontend Masters

# Packages

E tudo começa com o comando de `go mod init`, ao qual torna o projeto um novo módulo. No Go, basicamente tudo é módulo, e dentro desse módulo há os `packages`.

Podemos considerar que cada pasta é um package e assim por diante, mas o principal é manter em foco essa organização.

## Nomenclatura

O nome desse módulo pode partir desde uma URL, como também simplesmente um nome. Essa URL não precisa, necessariamente existir ainda, mas o importante é sempre manter o padrão.

Esse mesmo nome é usado no comando que inicializa o Módulo. Sendo assim, damos o comando de `go mod init packages-in-go.com/go/packages`, por exemplo, e pronto, módulo criado.

## Mudança de planos

Caso a nomenclatura mude, é simples corrigir. Basta ir ao arquivo `go.mod` na raiz do projeto e realizar essa mudança. Essa linguagem é feita para ser simples, sendo assim, essea arquivo vai guardar os metadados do projeto, e basta então realizar essa mudança que já está tudo certo.

# Getting Started

Então, para que o programa inicie e tudo o que foi feito rode corretamente, precisamos sempre de um arquivo raiz `.go`, e dentro desse arquivo a definição do `package main` com a `main()`.

Sendo assim, ao rodar o código de [`main.go`](./main.go) com o comando `go run main.go`, o `"Hey!"` vai ser printado em tela.

## Disclaimer

É primordial que haja apenas um único arquivo que define o `package main` e possui a função `main()`.

Para exemplificar, dupliquei o [`main.go`](./main.go) e criei o [`app.go`](./app.go), e com isso, ao abrir um arquivo, já é acusado o erro de que a referência à `main` está duplicada.