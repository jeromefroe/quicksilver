# Quicksilver

An experiment using [gorun] to execute Go programs as scripts. To execute a Go program as a
script, make it executable and then call it like any other program:

```bash
$ chmod +x hello.go
$ ./hello.go
Hello world!
```

## Caveats

Go won't be able to compile the file normally because of the shebang at the start of it:

```bash
$ go build hello.go
can't load package: package main:
hello.go:1:1: illegal character U+0023 '#'
```

[gorun]: https://github.com/erning/gorun
