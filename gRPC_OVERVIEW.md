# gRPC
## Overview
### Why use gRPC
- Large-scale distributed systems actually composed of microservices
- Multi-language, multi-platform framework
- Transport over HTTP/2 + TLS
- Generic low level API in C
### gRPC in a nutshell
#### IDL to describe service API
##### Protocol Buffers IDL
Define a service in a .proto file using Protocol Buffers IDL
```xml
syntax = "proto3";

message Book {
  string name = 1;
  int32 id = 2;
  string author = 3;
  int32 ISBN = 4;
}

message BookId {
    int32 id = 2;
}

message Ack {
    int32 book = 5;
}

service BookShelf {
  rpc getBook(BookId) returns (Book);
  rpc insertBook(Book) returns (Ack);
}
```
-   Generate server and client stub code using the protocol buffer complier
-   Moreover, it also help data serialization
#### Automatically generate client stub and abstract server classes in 10+ languages
#### Take advantage of feature set of HTTP/2
#### C core
-   Include a full HTTP/2 transport implementation with authentication, etc
-   Manages interaction with system
-   Receives asynchronous event notifications (socket vents, timers)
-   Provides interface to wrapped-language stack
-   Not intended as an application-lever API
    *   Because of no support for protobufs

## Example
### Book Manager
Client be able to insert, get information a book in database.
Link project:
```html
https://github.com/conglb/Book-API-3.0
```
