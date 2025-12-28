# The Nodepp Project: Revolutionizing the World of Programming

### Redefining the World of Programming: Innovation Meets Simplicity.

Welcome to the exciting realm of Nodepp, where we bridge the gap between the raw power of C++ and the exhilarating simplicity of Node.js. In an ever-evolving digital landscape, we believe programming should be a high-speed adventure, not a struggle with convoluted syntax.

## Our Mission

The Nodepp Project isn't just another set of libraries; it’s a groundbreaking paradigm shift. We are dedicated to empowering developers from frontend wizards to back-end gurus to create robust, scalable, and efficient applications with unparalleled ease. Don't trust us? just take a look at our `hello-world http server` looks like:

```cpp
#include <nodepp/nodepp.h>
#include <nodepp/http.h>
#include <nodepp/date.h>

using namespace nodepp;

void onMain(){

    auto server = http::server([=]( http_t cli ){ 

        console::log( cli.path, cli.get_fd() );
        
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

At the heart of our project lies a commitment to streamlining the development process. We meticulously design our ecosystem to be intuitive, efficient, and beginner-friendly, while maintaining the extreme performance that only C++ can provide.

- **100% Asynchronous:** Harness the power of event-driven programming and non-blocking I/O.
- **Modular by Design:** A lightweight architecture with an extensive library of modules for Web, IoT, and Desktop.
- **Zero-Copy Logic:** Sophisticated memory management that works on everything from an Arduino Nano to a Cloud Server.

## Nodepp in Action
### Asynchronous Enigma Machine
https://github.com/user-attachments/assets/9b870671-3854-444f-893d-40fdce31a629

Try it now: [Enigma Machine Simulation](https://wokwi.com/projects/449104127751150593)

### Cursed-Luna (WASM Remake)
https://github.com/user-attachments/assets/3647b5b6-fbfd-4281-af0f-f35f3260a319

Play it now: [Cursed-Luna on Itch.io](https://edbcrepo.itch.io/cursed-luna)

### Duck Hunt VR (WASM Edition)
https://github.com/user-attachments/assets/ab26287e-bd73-4ee8-941b-d97382e203c9

Play it now: [Duck Hunt VR on Itch.io](https://edbcrepo.itch.io/duck-hunt-vr)

## Ecosystem

Whether you are building a real-time game, a secure network server, or a DIY hardware project, Nodepp is your trusted companion:

- 📌: **Nodepp Core:** The heart of the async framework.
- 📌: **Nodepp-Arduino:** Async power for microcontrollers.
- 📌: **Nodepp-WASM:** High-performance C++ in the browser.

The Nodepp Project is here to transform your coding experience. Embrace the future of programming, unlock your full potential, and join a community that is setting the projects of tomorrow in motion today.

**Get ready to code like never before!** 🫠

# Contribution

If you want to contribute to Nodepp, you are welcome to do so! You can contribute in several ways:

    ☕ Buying me a Coffee
    📢 Reporting bugs and issues
    📝 Improving the documentation
    📌 Adding new features or improving existing ones
    🧪 Writing tests and ensuring compatibility with different platforms
    🔍 Before submitting a pull request, make sure to read the contribution guidelines.


[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/edbc_repo)

# License
Nodepp is distributed under the MIT License. See the LICENSE file for more details.
