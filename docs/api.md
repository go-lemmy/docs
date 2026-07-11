# API reference

Source-verified against [`go-lemmy/lemmy`](https://github.com/go-lemmy/lemmy). The
authoritative, versioned reference is
[pkg.go.dev/github.com/go-lemmy/lemmy](https://pkg.go.dev/github.com/go-lemmy/lemmy).

## Constructor & methods

| Symbol | Purpose |
|---|---|
| `New(instance string, ...Option) *Client` | Construct a client for a Lemmy instance URL. |
| `(*Client).Posts(ctx, PostsOptions) (*PostList, error)` | List posts for a community / sort / page. |
| `(*Client).Login(ctx, usernameOrEmail, password) error` | Store a JWT for authenticated reads. |

## Options

Functional options passed to `New`:

| Option | Purpose |
|---|---|
| `WithHTTPClient(*http.Client)` | Supply a custom HTTP client (timeouts, transport). |
| `WithUserAgent(ua)` | Set the `User-Agent` header. |

## Result types

| Type | Purpose |
|---|---|
| `PostsOptions` | Query parameters (`Community`, `Sort`, `Limit`, …). |
| `Post` | A single post (`Title`, `Community`, `Score`, …). |
| `PostList` | A page of posts. |

!!! note
    This table is a map, not the contract. Field-level details live in the
    [package reference](https://pkg.go.dev/github.com/go-lemmy/lemmy) and the
    repository's `README`.
