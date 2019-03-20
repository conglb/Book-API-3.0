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
```angular2html

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


