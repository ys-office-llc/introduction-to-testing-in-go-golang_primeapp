# Introduction to Testing in Go (Golang)

## How to running test for golang

- command and args
```text
go test -v .
```
- result
```text
=== RUN   Test_isPrime
--- PASS: Test_isPrime (0.00s)
PASS
ok      primeapp        (cached)
```
- with cover

```text
$ go test -cover .
```
- result
```text
ok      primeapp        0.001s  coverage: 54.5% of statements
```
- with coverprofile
```text
go test -coverprofile=coverage.out
```
- convert html
```text
go tool cover -html=coverage.out 
```
- alias
```bash
alias coverage='go test -coverprofile=coverage.out && go tool cover -html=coverage.out'
```