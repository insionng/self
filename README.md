# Self
Just Myself Context for Martini.

## Description
`Self` provides a [web.go][] compitable layer for reusing the code written with
hoisie's `web.go` framework. Here compitable means we can use `Self` the same 
way as in hoisie's `web.go` but not the others.

## Usage

~~~ go
package main

import (
	"github.com/insionng/self"
	"log"
	"os"
)

func main() {
	l, e := os.Create("./self.Classico.log")
	if e != nil {
		log.Fatal(e.Error())
	}
	defer l.Close()

	m := self.Classico(l)
	m.Get("/", func(self *self.Context) {
		self.WriteString("Hello , Hello , Hello , World!")
	})

	m.Run()
}


~~~

## Authors
* [Insion Ng](http://github.com/insionng)
* [Jeremy Saenz](http://github.com/codegangsta)
* [Archs Sun](http://github.com/Archs)
* [hoisie](https://github.com/hoisie)

## Links
* [Self Martini](http://github.com/insionng/self)
* [Selfor Marcaron](http://github.com/insionng/selfor)
