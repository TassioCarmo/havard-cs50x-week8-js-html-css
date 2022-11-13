# Introduction to javascript, html and CSS
## what did i learn

## internet 
is the network of networks of computers, or servers, communicating with one another by sending and receiving data. 

## router
Are specialized computers, with CPUs and memory, that routes, or relays, data from one point to another. 
and as the name implies, just routes data left to right, top to bottom, from one point to another
A router might have multiple options for what direction to send some data, and there are algorithms that try to figure out that direction.

there's algorithms that figure out how you decide to send a packet up, down, left, or right, so to speak. But they do so by taking an input

## TCP/IP
the message would have the source address and the destination address and the type of server, garantees the package will get to the destination

are two protocols for sending data between two computers. In the real world, we might write an address on an envelope in order to send a letter to someone, along with our own address for a letter in return.
 
### IP
stands for internet protocol, a protocol that includes a standard way for computers to address each other. IP addresses are unique addresses for computers connected to the internet, such that a packet sent from one computer to another will be passed along routers until it reaches its destination.

An IP address might have the format #.#.#.#, where each number can have a value from 0 to 255. Each number will be the size of one byte, so the entire address will be 4 bytes, or 32 bits. This means that this version of IP, version 4, can only support a maximum of 4 billion addresses. Another version of IP, version 6, uses 128 bits to support many more possible addresses.

### TCP

transmission control protocol, is a protocol for sending and receiving data. TCP allows for a single server, at the same IP address, to provide multiple services through the use of a port number, a small integer added to the IP address. For example, HTTP is sent to port number 80, and HTTPS uses port number 443.

- TCP also allows for a large amount of data, like an image, to be sent in smaller chunks. Each of them might be labeled with a sequence number, as with “part 1 of 4” or “part 2 of 4”. And if one of the parts is lost, the recipient can ask for the missing part again.
- UDP is another protocol for sending data that does not guarantee delivery like TCP, which might be useful for streaming real-time videos or calls, since we don’t want to wait for all the packets to be redelivered before we get new ones.


Two commands supported by HTTP include GET and POST. GET allows a browser to ask for a page or file in a URL, and POST allows a browser to send additional data to the server that is hidden from the URL. Both of these are requests we can make to a server, which will provide a response in return.

## DNS Domaon name system

cs50.harvard.edu to IP addresses. DNS is generally provided by a server nearby, with a big table in its memory, of domain names and IP addresses.

Translate domain names to IP addresses

## HTTP, or Hypertext Transfer Protocol, 
standardizes how web browsers and web servers communicate within TCP/IP packets.

   HTTPS is the secure version of HTTP, ensuring that the contents of packets between the browser and server are encrypted.
   
   
 URL, or web address, might look like https://www.example.com/.

 - https:// is the protocol being used.
 - The / at the end is a request for the default file. It might also end in something like /file.html for a specific file.
 - example.com is the domain name. .com is a top-level domain name, and others like .edu or .io indicate what type of website might be hosted there. Today, there are hundreds of top-level domain names, some with restrictions on how they can be used.
 - www is the hostname, or subdomain, that refers to one or more specific servers in the domain name. A domain name might include web servers for www, or email servers for mail, so each subdomain can point to them separately.
 - Together, www.example.com is a fully qualified domain name, or one that has a specific set of addresses.


GET request will start with:

GET / HTTP/1.1
Host: www.example.com

- The GET indicates that the request is for some file, and / indicates the default file.
- There are different versions of the HTTP protocol, so HTTP/1.1 indicates that the browser is using version 1.1.
- Host: www.example.com indicates that the request is for www.example.com, since the same web server might be hosting multiple websites and domains.

response for a successful request will start with:

HTTP/1.1 200 OK
Content-Type: text/html


- The web server will respond with the version of HTTP, followed by a status code, which is 200 OK here, indicating that the request was valid.
- Then, the web server indicates the type of content in its response, which might be text, image, or other format.
- Finally, the rest of the packet or packets will include the content.


HTTP status codes include:

    200 OK
    301 Moved Permanently
    302 Found
    304 Not Modified
    307 Temporary Redirect
    401 Unauthorized
    403 Forbidden
    404 Not Found
    418 I'm a Teapot
        An April Fool’s joke years ago
    500 Internal Server Error
        Buggy code on a server might result in this status code, like segfaults we might have seen in C.
    503 Service Unavailable

## HTML

HTML, Hypertext Markup Language, is not a programming language, but rather used to format web pages and tell the browser how to display them.

it's just tags and attributes that you don't need to remember 100% of the time

server with the <code>http-server</code> command, and clicking “Open in Browser” in the notification that appears.

- The first line, <!DOCTYPE html>, is a declaration that the page follows the HTML standard.
- Next is a tag, a word in brackets like <html> and </html>. The first is a start or open tag, and the second is a close tag, which looks almost the same but with a / in front of the tag’s name. In this case, the tags indicate the start and end of the HTML page. The start tag here has an attribute as well, lang="en" which specifies that the language of the page will be in English, to help the browser translate the page if needed. Notice that attributes are key-value pairs.
- Nested within the <html> tag are two more tags, <head> and <body>, which are both like children nodes in a tree. And within <head> is the <title> tag, the contents of which we see in a tab or window’s title in a browser. Within <body> is the contents of the page itself, a text node, which we’ll see in the main view of a browser as well.

 Element: start tag and end tag and everything in between
 
 Pure text in HTMl is called text node
 
 ![image](https://user-images.githubusercontent.com/31789624/201429134-fdd1ee23-3dea-4340-be50-58b5e4665cf0.png
 
### List
 ```
 <!DOCTYPE html>

<html lang="en">
    <head>
        <title>list</title>
    </head>
    <body>
        <ul>
            <li>foo</li>
            <li>bar</li>
            <li>baz</li>
        </ul>
    </body>
</html>
```
### Table
 ```
         <table>
            <thead>
                <tr>
                    <th>Name</th>
                    <th>Number</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>Carter</td>
                    <td>+1-617-495-1000</td>
                </tr>
                <tr>
                    <td>David</td>
                    <td>+1-949-468-2750</td>
                </tr>
            </tbody>
        </table>
```
 
### Image
 ```
      <img alt="Harvard University" src="harvard.jpg">
 ```
### Video
 ```
 <video autoplay loop muted width="1280">
            <source src="halloween.mp4" type="video/mp4">
 </video>
 ```
### embed another page in ours with an inline frame, or iframe: 
 
 ```
         <iframe allowfullscreen src="https://www.youtube.com/embed/xvFZjo5PgG0"></iframe>
 ```
 
### responsive, or automatically adapted for different screen sizes:

```
     <meta name="viewport" content="initial-scale=1, width=device-width">
```

## URL
 
 URL can change when you do a search for example to include the user's input. This is how humans provide input to servers. They don't manually create the URLs, like I sort of just did. 

when you fill out a form on the web and you hit Enter, typically the URL suddenly changes to include whatever you typed in, in the URL, assuming the form is using the verb GET. That's not ideal. If you're typing in a username, a password, a credit card information, because you don't want the next person to sit down at your laptop to see literally everything you typed in, saved in your history. So there's another verb, POST, that can hide all of that. 

 ## Dev tool
 
 ![image](https://user-images.githubusercontent.com/31789624/201502139-5b085b9b-f271-4b0d-aa32-c3e9f8f92aa2.png)

 
 Example of search
 ```
 <!DOCTYPE html>

<html lang="en">
    <head>
        <title>search</title>
    </head>
    <body>
        <form action="https://www.google.com/search" method="get">
            <input name="q" type="text">
            <input type="submit">
        </form>
    </body>
</html>

```
