## listpushback

### Instructions

Écrire une fonction `ListPushBack` qui insère un nouvel élément `NodeL` au début de la liste `l` en utilisant la structure `List`.

### Fonction et structue attendues

```go
type NodeL struct {
	Data interface{}
	Next *NodeL
}

type List struct {
	Head *NodeL
	Tail *NodeL
}

func ListPushFront(l *List, data interface{}) {
}
```

### Utilisation

Voici un éventuel [programme](TODO-LINK) pour tester votre fonction :

```go
package main

import (
	piscine ".."
	"fmt"
)

func main() {

	link := &piscine.List{}

	piscine.ListPushFront(link, "Hello")
	piscine.ListPushFront(link, "man")
	piscine.ListPushFront(link, "how are you")

	it := link.Head
	for it != nil {
		fmt.Println(it.Data)
		it = it.Next
	}
}
```

Et son résultat :

```console
student@ubuntu:~/piscine-go/test$ go build
student@ubuntu:~/piscine-go/test$ ./test
how are you
man
Hello
student@ubuntu:~/piscine-go/test$
```
