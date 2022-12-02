
```go
$ go doc log
```

***

[log package](https://pkg.go.dev/log#pkg-index)

```go
Constants
func Fatal(v ...any)
func Fatalf(format string, v ...any)
func Fatalln(v ...any)
func Flags() int
func Output(calldepth int, s string) error
func Panic(v ...any)
func Panicf(format string, v ...any)
func Panicln(v ...any)
func Prefix() string
func Print(v ...any)
func Printf(format string, v ...any)
func Println(v ...any)
func SetFlags(flag int)
func SetOutput(w io.Writer)
func SetPrefix(prefix string)
func Writer() io.Writer
...
```

***

# Examples
[Logging Go Programs](https://www.golangprograms.com/go-language/logging-go-programs.html)

```go
// Program in GO language to demonstrates how to use base log package.
package main

import (
	"log"		
)

func init(){
	log.SetPrefix("LOG: ")
	log.SetFlags(log.Ldate | log.Lmicroseconds | log.Llongfile)
	log.Println("init started")
}

func main() {
  	// Println writes to the standard logger.
	log.Println("main started")

  	// Fatalln is Println() followed by a call to os.Exit(1)
	log.Fatalln("fatal message")

  	// Panicln is Println() followed by a call to panic()
	log.Panicln("panic message")
}
```
***
