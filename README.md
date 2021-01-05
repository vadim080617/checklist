# Checklist

 <table>
    <tr>
        <td>:white_medium_small_square: <a href="#http">HTTP</a></td>
    </tr>
    <tr>
        <td>:white_medium_small_square: <a href="#https">HTTPS</a></td>
    </tr>
    <tr>
        <td>:white_medium_small_square: <a href="#http-methods">HTTP methods</a></td>
    </tr>
    <tr>
        <td>:white_medium_small_square: <a href="#cors">Cors</a></td>
    </tr>
</table>

### Http
###### General information
 HTTP is a protocol which allows the fetching of resources, such as HTML documents. It is the foundation of any data exchange on the Web and it is a ***client-server protocol***, which means requests are initiated by the recipient, usually the Web browser. A complete document is reconstructed from the different sub-documents fetched, for instance text, layout description, images, videos, scripts, and more.
 
 Clients and servers communicate by exchanging individual messages (as opposed to a stream of data). The messages sent by the client, usually a Web browser, are called requests and the messages sent by the server as an answer are called responses.
 
 The *client* is any tool that acts on the behalf of the user. This role is primarily performed by the Web browser; other possibilities are programs used by engineers and Web developers to debug their applications.
 
 On the opposite side of the communication channel, is the *server*, which serves the document as requested by the client. A server appears as only a single machine virtually: this is because it may actually be a collection of servers, sharing the load (load balancing) or a complex piece of software interrogating other computers (like cache, a DB server, or e-commerce servers), totally or partially generating the document on demand.


###### Basic aspects of HTTP
 - HTTP is simple (human readable)
 - HTTP is extensible (new functionality - new headers)
 - HTTP is stateless, but not sessionless (no link between 2 requests, add session cookie to each request)

###### HTTP flow
- Open a TCP connection
- Send an HTTP message
- Read the response sent by the server
- Close or reuse the connection for further requests.

:information_source: More information [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)

<p><a href="#checklist">Back to top :arrow_double_up:</a></p>

- - - 
### Https
HTTPS (Hypertext Transfer Protocol Secure) is an internet communication protocol that protects the integrity and confidentiality of data between the user's computer and the site. Users expect a secure and private online experience when using a website.

Data sent using HTTPS is secured via Transport Layer Security protocol (TLS), which provides three key layers of protection:
1. **Encryption** - encrypting the exchanged data to keep it secure from eavesdroppers. That means that while the user is browsing a website, nobody can "listen" to their conversations, track their activities across multiple pages, or steal their information.
2. **Data integrity** - data cannot be modified or corrupted during transfer, intentionally or otherwise, without being detected.
3. **Authentication** - proves that your users communicate with the intended website. It protects against man-in-the-middle attacks and builds user trust, which translates into other business benefits.

:information_source: More information:
 - [Developers google](https://developers.google.com/search/docs/advanced/security/https)
 - [Wiki](https://en.wikipedia.org/wiki/HTTPS)

<p><a href="#checklist">Back to top :arrow_double_up:</a></p>

- - -
### Http methods
- **GET**  
Requests a representation of the specified resource. Requests using GET should only retrieve data.
- **HEAD**  
Asks for a response identical to that of a GET request, but without the response body.
- **POST**  
Submit an entity to the specified resource, often causing a change in state or side effects on the server.
- **PUT**  
Replaces all current representations of the target resource with the request payload.
- **DELETE**  
Deletes the specified resource.
- **CONNECT**  
Establishes a tunnel to the server identified by the target resource.
- **OPTIONS**  
Describe the communication options for the target resource.
- **TRACE**  
Performs a message loop-back test along the path to the target resource.
- **PATCH**  
Apply partial modifications to a resource.

In the REST API:
|Method|Used for|URL|
|------|-------|----|
|GET|Get entity or list of entities|`/books/1` *or* `/books`|
|POST|Create entity|`/books`|
|PUT|Replace entity|`/books/1`|
|PATCH|Update entity|`/books/1`|
|DELETE|Delete entity|`/books/1`|

**Options** methods usually used for preflight request. (CORS)

:information_source: More information [here](https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods)

<p><a href="#checklist">Back to top :arrow_double_up:</a></p>

- - -
### Cors

**Cross-Origin Resource Sharing** (CORS) is an HTTP-header based mechanism that allows a server to indicate any other origins (domain, scheme, or port) than its own from which a browser should permit loading of resources. CORS also relies on a mechanism by which browsers make a “preflight” request to the server hosting the cross-origin resource, in order to check that the server will permit the actual request. In that preflight, the browser sends headers that indicate the HTTP method and headers that will be used in the actual request.

The CORS protocol consists of a set of headers that indicates whether a response can be shared cross-origin.

For requests that are more involved than what is possible with HTML’s form element, a CORS-preflight request is performed, to ensure request’s current URL supports the CORS protocol.

An example of a cross-origin request: the front-end JavaScript code served from `https://domain-a.com` uses XMLHttpRequest to make a request for `https://domain-b.com/data.json`.

For security reasons, browsers restrict cross-origin HTTP requests initiated from scripts. For example, XMLHttpRequest and the Fetch API follow the same-origin policy. This means that a web application using those APIs can only request resources from the same origin the application was loaded from unless the response from other origins includes the right CORS headers.

:information_source: More information:
 - [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS) // highly recommend read this article in full
 - [Specification](https://fetch.spec.whatwg.org/#cors-protocol)

 <p><a href="#checklist">Back to top :arrow_double_up:</a></p>

- - -
