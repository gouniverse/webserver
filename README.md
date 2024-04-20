# Web Server

<a href="https://gitpod.io/#https://github.com/gouniverse/webserver" style="float:right;" target="_blank"><img src="https://gitpod.io/button/open-in-gitpod.svg" alt="Open in Gitpod" loading="lazy"></a>

![tests](https://github.com/gouniverse/webserver/workflows/tests/badge.svg)
[![Go Report Card](https://goreportcard.com/badge/github.com/gouniverse/webserver)](https://goreportcard.com/report/github.com/gouniverse/webserver)
[![PkgGoDev](https://pkg.go.dev/badge/github.com/gouniverse/webserver)](https://pkg.go.dev/github.com/gouniverse/webserver)

## Description
Predefined web server

## Usage

```go
srv := New("localhost:45568", func(w http.ResponseWriter, r *http.Request) {
    w.WriteHeader(http.StatusOK)
    w.Write([]byte("Hello world"))
})

err := srv.Start()
if err != nil {
    t.Error("server error:", err)
}
```