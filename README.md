# MadMod
The golang MadPin's Module madmod

That's part of the study, that' I've started at [study golang basic](https://github.com/madpin/study-golang-basic).  

I'm following the [create module](https://go.dev/doc/tutorial/create-module) guide.

Starting the module:
```bash
go mod init github.com/madpin/madmod
```

Since the tutorial is for greetings, let's start with that:  
Creating file: `greetings.go`
```go
package greetings

import "fmt"

// Hello returns a greeting for the named person.
func Hello(name string) string {
    // Return a greeting that embeds the name in a message.
    message := fmt.Sprintf("Hi, %v. Welcome!", name)
    return message
}
```