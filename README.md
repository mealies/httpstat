# httpstat [![Build Status](https://github.com/mealies/httpstat/actions/workflows/push.yml/badge.svg)](https://github.com/mealies/httpstat/actions/workflows/push.yml) [![Go Report Card](https://goreportcard.com/badge/github.com/mealies/httpstat)](https://goreportcard.com/report/github.com/mealies/httpstat)

![Shameless](./screenshot.png)

Imitation is the sincerest form of flattery.

This is a copy of Dave Cheney's go version of [httpstat](https://github.com/davecheney/httpstat) changed to include support for HTTP3
## Installation
`httpstat` requires Go 1.24 or later.
```
go install github.com/mealies/httpstat@latest
```

## Usage
```
httpstat https://example.com/
```
## Features

- HTTP3 support
- Windows/BSD/Linux supported.
- HTTP and HTTPS are supported, for self-signed certificates use `-k`.
- Skip timing the body of a response with `-I`.
- Follow 30x redirects with `-L`.
- Change HTTP method with `-X METHOD`.
- Provide a `PUT` or `POST` request body with `-d string`. To supply the `PUT` or `POST` body as a file, use `-d @filename`.
- Add extra request headers with `-H 'Name: value'`.
- The response body is usually discarded, you can use `-o filename` to save it to a file, or `-O` to save it to the file name suggested by the server.
- HTTP/HTTPS proxies supported via the usual `HTTP_PROXY`/`HTTPS_PROXY` env vars (as well as lower case variants).
- Supply your own client side certificate with `-E cert.pem`.

