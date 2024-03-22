# modul-6-adpro

**Commit 1**
The Rust function `handle_connection` is tailored to manage TCP connections, focusing particularly on parsing and presenting HTTP request headers. It employs `TcpStream` to establish the connection and `BufReader` for streamlined reading. Within the function, it iterates through lines from the connection until it reaches the conclusion of the HTTP headers, then compiles and outputs these headers.