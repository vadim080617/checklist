# Checklist

 <table>
    <tr>
        <td>:white_medium_small_square: <a href="#http">HTTP</a></td>
    </tr>
    <tr>
        <td>:white_medium_small_square: <a href="#https">HTTPS</a></td>
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
HTTPS (Hypertext Transfer Protocol Secure) is an internet communication protocol that protects the integrity and confidentiality of data between the user's computer and the site. Users expect a secure and private online experience when using a website. We encourage you to adopt HTTPS in order to protect your users' connections to your website, regardless of the content on the site.

Data sent using HTTPS is secured via Transport Layer Security protocol (TLS), which provides three key layers of protection:
1. **Encryption** - encrypting the exchanged data to keep it secure from eavesdroppers. That means that while the user is browsing a website, nobody can "listen" to their conversations, track their activities across multiple pages, or steal their information.
2. **Data integrity** - data cannot be modified or corrupted during transfer, intentionally or otherwise, without being detected.
3. **Authentication** - proves that your users communicate with the intended website. It protects against man-in-the-middle attacks and builds user trust, which translates into other business benefits.

:information_source: More information:
 - [Developers google](https://developers.google.com/search/docs/advanced/security/https)
 - [Wiki](https://en.wikipedia.org/wiki/HTTPS)

<p><a href="#checklist">Back to top :arrow_double_up:</a></p>

- - -