# modul-6-adpro

**Commit 1**

The Rust function `handle_connection` is tailored to manage TCP connections, focusing particularly on parsing and presenting HTTP request headers. It employs `TcpStream` to establish the connection and `BufReader` for streamlined reading. Within the function, it iterates through lines from the connection until it reaches the conclusion of the HTTP headers, then compiles and outputs these headers.

**Commit 2**

Modifying the `handle_connection` function to display a basic HTML page provided valuable insights into the process of delivering content to a web browser. Previously, the code merely examined the web request without taking significant action. However, the updated function now effectively delivers an actual web page that is visible in our browser. This experience enlightened me on the communication between a server and a browser, adhering to specific protocols such as responding with "OK" to confirm smooth operation and indicating the page size to help the browser anticipate data. Furthermore, it demonstrated the utilization of Rust to access a file and transmit its content over the internet.
![Commit 2 screen capture](commit2.png)

**Commit 3**

I included a new HTML file called oops.html to serve as the 404 Not Found page. Subsequently, I adjusted the handle_connection function within our HTTP server. This updated function scrutinizes the initial line of the client's HTTP request to verify whether it's a GET/HTTP/1.1 request, indicating a request for the root path (/). If this condition is met, it replies with the status line HTTP/1.1 200 OK and delivers the content of the hello.html file. Conversely, if it detects otherwise, it issues a HTTP/1.1 404 NOT FOUND status line and delivers the content of the notfound.html file.
![Commit 3 screen capture](commit3.png)