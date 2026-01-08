# The Nodepp Project: A Unified Asynchronous World for C++

### Bridging the Gap Between C++ Performance and Node.js Simplicity.

Nodepp is a unified C++ framework designed to simplify high-performance asynchronous programming. By combining an **Event-Driven Reactor** with an **EE-inspired memory model**, Nodepp allows you to write C++ using a familiar, non-blocking syntax that scales from 8-bit microcontrollers to multi-core cloud servers.

We believe that programming should be a high-speed adventure, not a struggle with fragmented libraries or convoluted syntax.

## The Nodepp Philosophy: "Write Once, Compile Everywhere"

Unlike traditional C++ development that relies on **gluing** independent libraries together, Nodepp is **Vertically Integrated**. This **Unified World** architecture ensures that every module — from JSON parsers to HTTP servers — shares the same DNA:

- **100% Asynchronous:** Native I/O Multiplexing (Epoll, IOCP, Kqueue) for massive concurrency.
- **Mechanical Sympathy:** Memory primitives designed for cache efficiency and zero-copy data propagation.
- **Hardware Agnostic:** The exact same code runs on an Arduino Nano, WebAssembly, or Linux/Windows.

## Hello World: High-Performance HTTP
Nodepp abstracts the complexity of socket management, headers, and timing into a clean, intuitive API.

```cpp
#include <nodepp/nodepp.h>
#include <nodepp/http.h>
#include <nodepp/date.h>

using namespace nodepp;

void onMain(){

    auto server = http::server([=]( http_t cli ){ 

        console::log( "request: ", cli.path );
        
        cli.write_header( 200, header_t({
            { "content-type", "text/html" }
        }));
        
        cli.write( date::fulltime() );

    });

    server.listen( "localhost", 8000, [=]( socket_t server ){
        console::log("server started at http://localhost:8000");
    });

}
```

## Proof of Concept: Multi-Platform Execution

### Asynchronous Enigma Machine
Proving that 8-bit **bare metal** hardware can handle complex cryptographic rotations without blocking the system.

https://github.com/user-attachments/assets/9b870671-3854-444f-893d-40fdce31a629

Try it now: [Enigma Machine Simulation](https://wokwi.com/projects/449104127751150593)

### Cursed-Luna
A high-performance remake showcasing tight gameplay mechanics and efficient state management.

https://github.com/user-attachments/assets/3647b5b6-fbfd-4281-af0f-f35f3260a319

Play it now: [Cursed-Luna on Itch.io](https://edbcrepo.itch.io/cursed-luna)

### Duck Hunt VR
Low-latency VR natively in the browser. Low-level C++ performance meeting modern Web APIs.

https://github.com/user-attachments/assets/ab26287e-bd73-4ee8-941b-d97382e203c9

Play it now: [Duck Hunt VR on Itch.io](https://edbcrepo.itch.io/duck-hunt-vr)

## One Codebase, Every Screen
Nodepp is the only framework that lets you share logic between the deepest embedded layers and the highest web layers.

- **Hardware:** [NodePP for Arduino](https://github.com/NodeppOfficial/nodepp-arduino)
- **Desktop:** [Nodepp for Desktop](https://github.com/NodeppOfficial/nodepp)
- **Browser:** [Nodepp for WASM](https://github.com/NodeppOfficial/nodepp-wasm)

## Contributing

The Nodepp Project is an open-source research effort into deterministic, unified systems. Whether you are a frontend wizard or a backend guru, your contribution helps set the projects of tomorrow in motion.

- **Sponsorship:** Support the project via [Ko-fi](https://ko-fi.com/edbc_repo).
- **Bug Reports:** Open an issue via GitHub.
- **License:** MIT.

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/edbc_repo)

## License
**Nodepp** is distributed under the MIT License. See the LICENSE file for more details.
