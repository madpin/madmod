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

## Errors
That was nice and all, but let's change `greetings` to `madmod` right? =]  

Plus, some more changes to the now: `madmod.go`:
```go
package madmod

import (
	"errors"
	"fmt"
)

// Hello returns a greeting for the named person.
func Hello(name string) (string, error) {
	// If no name was given, return an error with a message.
	if name == "" {
		return "", errors.New("empty name")
	}

	// If a name was received, return a value that embeds the name
	// in a greeting message.
	message := fmt.Sprintf("Hi, %v. Welcome!", name)
	return message, nil
}
```

