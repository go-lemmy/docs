# go-lemmy

Pure-Go read client for the Lemmy REST API.

A pure-Go (**CGO=0**), dependency-free read client for the [Lemmy](https://join-lemmy.org/) REST API (`/api/v3`). Point it at any Lemmy instance and read its communities and posts. An optional `Login` stores a JWT for authenticated reads. Standard library only; builds for all 64-bit targets.

## Install

```sh
go get github.com/go-lemmy/lemmy
```

## At a glance

- **CGO-free** (`CGO_ENABLED=0`), Go 1.26+ — builds for every 64-bit target.
- **Zero third-party dependencies** — standard library only.
- **Read-only** — this is a read client; it does not post or mutate.
- BSD-3-Clause.

See [Usage](usage.md) for a runnable example and [API reference](api.md) for the
full surface. The canonical, always-current reference is
[pkg.go.dev](https://pkg.go.dev/github.com/go-lemmy/lemmy).
