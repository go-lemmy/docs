# Usage

```go
package main

import (
	"context"
	"fmt"

	"github.com/go-lemmy/lemmy"
)

func main() {
	c := lemmy.New("https://lemmy.world")

	list, err := c.Posts(context.Background(), lemmy.PostsOptions{
		Community: "technology", Sort: "Hot", Limit: 20,
	})
	if err != nil {
		panic(err)
	}
	for _, p := range list.Posts {
		fmt.Printf("%s — %s (score %d)\n", p.Title, p.Community, p.Score)
	}
}
```

`New` takes the instance base URL. `PostsOptions` selects the community, sort and page size. For authenticated reads, call `Login` first to store a JWT on the client.

For the complete, always-current API — every type and field — see
[pkg.go.dev/github.com/go-lemmy/lemmy](https://pkg.go.dev/github.com/go-lemmy/lemmy).
