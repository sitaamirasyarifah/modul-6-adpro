# modul-6-adpro

**Commit 1**

The Rust function `handle_connection` is tailored to manage TCP connections, focusing particularly on parsing and presenting HTTP request headers. It employs `TcpStream` to establish the connection and `BufReader` for streamlined reading. Within the function, it iterates through lines from the connection until it reaches the conclusion of the HTTP headers, then compiles and outputs these headers.

**Commit 2**

Modifying the `handle_connection` function to display a basic HTML page provided valuable insights into the process of delivering content to a web browser. Previously, the code merely examined the web request without taking significant action. However, the updated function now effectively delivers an actual web page that is visible in our browser. This experience enlightened me on the communication between a server and a browser, adhering to specific protocols such as responding with "OK" to confirm smooth operation and indicating the page size to help the browser anticipate data. Furthermore, it demonstrated the utilization of Rust to access a file and transmit its content over the internet.
![Commit 2 screen capture](commit2.png)

**Commit 3**

Certainly, here's a breakdown of the process into step-by-step instructions:

1. **Add a New HTML File:**
   - Create a new HTML file named "notfound.html" to serve as the 404 Not Found page.

2. **Update the HTTP Server Function:**
   - Modify the handle_connection function within your HTTP server.

3. **Inspect Request Type:**
   - Within the handle_connection function, examine the initial line of the client's HTTP request.

4. **Check Request Type:**
   - Verify whether the request is a GET/HTTP/1.1 request, indicating a request for the root path (/).

5. **Handle Request Type:**
   - If the request is a GET/HTTP/1.1 request:
     - Respond with the status line HTTP/1.1 200 OK.
     - Serve the contents of the hello.html file.

6. **Handle Other Request Types:**
   - If the request is not a GET/HTTP/1.1 request:
     - Issue a HTTP/1.1 404 NOT FOUND status line.
     - Serve the contents of the notfound.html file.

![Commit 3 screen capture](commit3.png)