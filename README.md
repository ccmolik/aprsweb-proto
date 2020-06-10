# aprsweb-proto

This package is meant to define an APRS checkin in Twirp schema format.

APRSWeb uses this schema for serializing messages into JSON and Protobuf.

For more information on Twirp, see [the docs](https://twitchtv.github.io/twirp/docs/intro.html)

## Building
Follow the [Twirp Installation Guide](https://twitchtv.github.io/twirp/docs/install.html), installing Golang, `protoc`, `protoc-gen-go`, and `protoc-gen-twirp`.
Make changes to `rpc/aprsweb/aprsweb.proto` and build the artifacts from the root of this directory as follows:

```
protoc --proto_path=. --twirp_out=. --go_out=. ./rpc/aprsweb/aprsweb.proto
```
## Why include the artifacts and not just the proto files?
Few people want to set up the `protoc` and `protoc-gen-*` packages you need to build these schemas on embedded devices (raspis.)

So, we version them with the repo.
