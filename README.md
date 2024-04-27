# Introduction to javascript, HTML and CSS

## what did i learn

### Summary: 

- **Internet:** cables connecting a network
- **Router:** Route information/packages to point A to B (imagine someone giving information to where you need to go) 
- **IP (Internet Protocol)**: Sender/Denstination address in other words Standardized how the adressed work, in others words governs how computers acess each other
- **TCP (Transmission Control Protocol):** "guaratees" delivery and helps the servers do more than one thing (email/web/video conference etc) in other words governs how computers track sequences of packets to point A to B
- **DNS (Domain Name System):** Server which answers what is the IP address for this domain name (www.x.com)
- **DHCP (Dynamic Host Configuration Protocol):** Assigns you an ip address/router
- **HTTP (Hypertext Transfer Protocol):** Governs how web browsers and web servers speak imagine a restaurant an browsers veing the costumer
- Two different ways to request information from a server/format request
   - GET: getting information ( cliking on links)
   - Post Setting information (upload a image or sending credit card information)

   ** Browser to server**
  ```
   GET / HTTP/2
  Host: www.harvard.edu
  ```
 - "/" (default page)
 - "HTTP/2" HTTPversion
 - "Host: something" what qualified domain you are looking for 

 **Server to Browser**
 ```
   HTTP/2 200
  Content-Type: text/html
```
- "HTTP/2" HTTPversion
- "200" status code showing the status of the request (ok)
-   Content-Type: text/html

- **Regular Expression** pattern the broswer should much the user input agaisnt and make sure it indeed matches
- .+@+\.edu

** Semantic tags ** 
- divs with clarifications header footer etc

## How to ask questions

Always Provide Your Code and the Surrounding Context
Ask About the Problem at Hand, Not the Solution Itself
Don’t Take Asking for More Context to Heart


## internet 
Is the network of networks of computers, or servers, communicating with one another by sending and receiving data. (aka a cable)

## Router
Are specialized computers, with CPUs and memory, that routes, or relays, data from one point to another. 

and as the name implies, just routes data left to right, top to bottom, from one point to another.

A router might have multiple options for what direction to send some data, and there are algorithms that try to figure out that direction.

there's algorithms that figure out how you decide to send a packet up, down, left, or right, so to speak. But they do so by taking an input

instead assign an IP address to a router. That router or access point just in your home, for example. 

## #Access Points
- One of the ways we’ve dealt with the IPv4 addressing problem is to start assigning multiple people to the same IP address.Today the router has the public address 
- while every device using it has the privates ,with the router's job as to sort of act as a traffic cop, allowing everybody who's connected to that router to use the same IP address to get out. 

## TCP/IP

 - ports: tells what is inside the package being send , a web request an email etc

- Resposible for getting it to the correct program, or the correct service on a machine. And it does something else that IP doesn't do, which is guarantee delivery. 
- in addition to specifying the **port** number, it also indicates how many packets, the internet protocol, IP, has split the data into. And it orders those packets so they can be reconstructed on the receiving machine, even if they received-- in a different order than they were sent. Which can happen because IP is a connectionless protocol, and so different packets can take different paths through the system. 
- Allows us to fragment data to be easier reasemble elsewhere

Are two protocols for sending data between two computers. In the real world, we might write an address on an envelope in order to send a letter to someone, along with our own address for a letter in return.

Commonly used that they have been standardized across all computers.
- FTP (file transfer) uses port 21.
- SMTP (e-mail) uses port 25.
- DNS uses port 53.
- HTTP (web browsing) uses port 80.
- HTTPS (secure web browsing) uses post 443.

IP gets those data chunks that have been wrapped with TCP, and wraps more information about where the packet is supposed to go. We might call this the IP layers surrounding the packet. 

We have the data in the middle, and then TCP on top of, telling it where the data inside of TCP is supposed to go, to what port or what service on a machine. Around that is the IP layer. What IP address, what machine, is actually getting this. 
 
### IP

Stands for internet protocol, a protocol that includes a standard way for computers to address each other. IP addresses are unique addresses for computers connected to the internet, such that a packet sent from one computer to another will be passed along routers until it reaches its destination.


In order for your machine to uniquely identify itself on the Internet, it needs an address.
- This way, it can send information out and also receive information back to the correct location.
- The addressing scheme used by computers is known as IP addressing.
- As originally developed, the IP addressing scheme would effectively allocate a unique 32-bit address to each device hoping to connect to the internet.
- Instead of representing these 32-bit addresses(roughly 4 billion addresses) as hexadecimal, we represent them as four clusters of 8-bits using decimal notation.
- Ex:140.247.223.81
- In recent years, we’ve been slowly phasing out this old scheme (IPv4) and replacing it with a newer scheme (IPv6) that assigns computers 128-bit addresses, instead of 32-bit addresses.

![image](https://user-images.githubusercontent.com/31789624/202000671-192cddd0-562e-4713-88c0-7badf1a17837.png)


the networks are not directly connected to each other at all, and rely on routers to distribute communications.
- On a small scale, this configuration may actually be more inefficient than just having direct connections.
- On a large scale, this configuration can dramatically reduce the costs of network infrastructure.
- IP is responsible for getting information from point A to point B and also breaking the information into small pieces so that the network isn't overly taxed. 

### DHCP Dynamic Host Configuration Protocol

Assigns you an ip address

### TCP

transmission control protocol, is a protocol for sending and receiving data. TCP allows for a single server, at the same IP address, to provide multiple services through the use of a port number, a small integer added to the IP address. For example, HTTP is sent to port number 80, and HTTPS uses port number 443.

- TCP also allows for a large amount of data, like an image, to be sent in smaller chunks. Each of them might be labeled with a sequence number, as with “part 1 of 4” or “part 2 of 4”. And if one of the parts is lost, the recipient can ask for the missing part again.
- UDP is another protocol for sending data that does not guarantee delivery like TCP, which might be useful for streaming real-time videos or calls, since we don’t want to wait for all the packets to be redelivered before we get new ones.


Two commands supported by HTTP include GET and POST. GET allows a browser to ask for a page or file in a URL, and POST allows a browser to send additional data to the server that is hidden from the URL. Both of these are requests we can make to a server, which will provide a response in return.

## DNS Domaon name system

cs50.harvard.edu to IP addresses. DNS is generally provided by a server nearby, with a big table in its memory, of domain names and IP addresses.



## Translate IP to domain names
```
Host             IPv4 Address
info.host1.net    0.0.0.0
info.host2.net    0.0.0.1
```
- DNS is really the local yellow pages. And large DNS servers like google.coms, they are actually just more like libraries that have a copy of all of the local yellow pages or all of the local DNS records. So there's really no one repository of the full DNS of the internet, just like there's no one yellow pages of the world. 

- There are all these local small scale DNSs that exist out there. And there are services that aggregate them together. But they depend on those smaller DNS systems updating their information, so that they have the most accurate information. 

## HTTP, or Hypertext Transfer Protocol
HTTP specifies/standardizes how exactly how one must make a request for a web page and exactly how a server, a machine that hosts web pages, delivers that information back to clients. 

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
 
- white space is data. And so when we're sending data from sender to receiver, from server to client, data costs money. And so getting rid of whitespace is actually a good idea if you're somebody who serves up a lot of web content. It's a bad idea if you're somebody who's learning this stuff and you want to have it nicely organized.

 <code> <!DOCTYPE html>< /b></code>
- Tells the browsers which version you are using 
 
 <code>< b>, < /b></code>
- Text between these tags will be rendered in boldfaceby the browser.
  
 <code>< i>, < /i></code>
- Text between these tags will be rendered in italicsby the browser.

 <code>< u>, < /u></code>
- Text between these tags will be rendered underlinedby the browser.

 <code>< p>, < /p></code>
- Text between these tags will be rendered as a paragraph by the browser, with space above and below.

 <code>< hX>, < /hX></code>
 X = 1, 2, 3, 4, 5, or 6
- Text between these tags will be rendered as an X-level section header.
 
 <code>< ul>, < /ul></code>
- Demarcate the beginning and end of an unordered (bulleted) list.

 <code>< ol>, < /ol></code>
- Demarcate the beginning and end of an ordered (numbered) list.

 <code>< li>, < /li></code>
- Demarcate list items with an ordered or unordered list.

 <code>< table>, < /table></code>
- Demarcate the beginning and end of a table definition.

 <code>< tr>, < /tr></code>
- Demarcate the beginning and end of a row within a table.

 <code>< td>, < /td></code>
- Demarcate the beginning and end of a column within a row within a table.

 <code>< form>, < /form></code>
- Demarcate the beginning and end of an HTML form.

 <code>< div>, < /div></code>
- Demarcate the beginning and end of an arbitrary HTML page division.

 <code>< input name=X type=Y /></code>
- Define a field within an HTML form. X is a unique identifier for that field, Y is what type of data it accepts.

 <code> < a href=X>, < /a></code>
- Creates a hyperlink to web page X, with the text between the tags rendered and functional as the link text.

 <code>< imgsrc=X ... /></code>
- Another self-closing tag for displaying an image located at X, with possible additionalattributes (such as specifying width and height).

 <code> < !DOCTYPE html></code>
- Specific to HTML5, lets the browser know that’s the standard you’re using.

 <code>< !--, -- ></code>
- Demarcate the beginning and end of an HTML comment.
 
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
 
## CSS
 Cascading Style Sheets, another language that tells our browser how to display tags on a page
 
 <code>< div></code> tags, or divisions, to indicate they are separate areas on our page.
  
  
common used
  
 <code> border: style color width</code>
- Applies a border of the specified color, width, and style (e.g., dotted, dashed, solid, ridge…).

 <code>background-color: [keyword | #<6-digit hex>]</code>
- Sets the background color. Some colors are pre-defined in CSS.

  <code>color: [keyword | #<6-digit hex>]</code>
- Sets the foreground color (usually text).
   
 <code>font-size: [absolute size | relative size] </code>
- Can use keywords (xx-small, medium…), fixed points (10pt, 12pt…), percentage (80%, 120%), or base off the most recent font size (smaller, larger).
 
   <code>font-family: [font name | generic name] </code>
- Certain “web safe” fonts are pre-defined in CSS.
 
   <code>text-align: [left | right | center | justify] </code>
- For displaying text.
 
## HTML entity
  
  <code>Copyright &#169; John Harvard</code>
  
## type selector 

### class selector: 
  
```
  html
          <header class="centered large">
   ----------
    Css
             .centered
            {
                text-align: center;
            }
 ```
### ID selector
 
```
 <p id="first">
  
  #first{
  
```
### first child
  ```
   
            p:first-child
            {
                font-size: larger;
            }
  ```
           
 ### link CSS file
           
           <code><link href="home.css" rel="stylesheet"></code>

  
    attribute selectors will affect tags with those attributes, and we can use a[href*="harvard.edu"] to be less specific in our selection, affecting tags with harvard.edu anywhere in its href.

## Frameworld
A set of CSS conventions and shared styles is known as a framework, with classes and components we can quickly use.
One popular framework is Bootstrap, with components like alerts that we can use with HTML like:
```
<div class="alert alert-warning">
    ...
</div>
```
    The framework provides the CSS that sets the style for those classes.

With the help of the documentation on Bootstrap’s website, we’ll include a <link> to its CSS for our page with a table:
```
<!DOCTYPE html>

<html lang="en">
    <head>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
        <title>table</title>
    </head>
    <body>
        <table class="table">
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
    </body>
</html>
```
    By adding the table class, per the Boostrap documentation, we see that our table is indeed stylized to be easier to read.

We’ll update our search page, too, with styles from Bootstrap:
```
<!DOCTYPE html>

<html lang="en">
    <head>
        <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-1BmE4kWBq78iYhFldvKuhfTAU6auU8tT94WrHftjDbrCEXSU1oBoqyl2QvZ6jIW3" crossorigin="anonymous">
    <title>search</title>
    </head>
    <body>
        <div class="container-fluid">

            <ul class="m-3 nav">
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://about.google/">About</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://store.google.com/">Store</a>
                </li>
                <li class="nav-item ms-auto">
                    <a class="nav-link text-dark" href="https://www.google.com/gmail/">Gmail</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link text-dark" href="https://www.google.com/imghp">Images</a>
                </li>
                <li class="nav-item">
                    <a class="btn btn-primary" href="https://accounts.google.com/ServiceLogin" role="button">Sign in</a>
                </li>
            </ul>

            <div class="text-center">
              <img alt="Happy Cat" class="img-fluid w-25" src="cat.gif">
              <form action="https://www.google.com/search" class="mt-4" method="get">
                  <input autocomplete="off" autofocus class="form-control form-control-lg mb-4 mx-auto w-50" name="q" placeholder="Query" type="search">
                  <button class="btn btn-light" type="submit">Google Search</button>
                  <button class="btn btn-light" name="btnI" type="submit">I'm Feeling Lucky</button>
              </form>
 
          </div>
        </div>
          
    </body>
</html>
```
# best practice. Stand on the shoulders of others as much as you can, using libraries. And then if you really don't like what the library is doing, then use your own skills and understanding of HTML and CSS to refine things a bit further.
           
           
## Javascript
 You can change in memory very interactive and dinamic
 
    
            The syntax of JavaScript is similar to that of C and Python for basic constructs:

```          
 setcounterto
0

let counter = 0;

changecounterby
1

counter = counter + 1;
counter += 1;
counter++;

ifx<
ythen

if (x < y)
{

}

ifx<
ythenelse

if (x < y)
{

}
else
{

}

ifx<ythenelseifx>
ythenelse

if (x < y)
{

}
else if (x > y)
{

}
else
{

}

forever

while (true)
{

}

repeat
3

for (let i = 0; i < 3; i++)
{

}
```


http-server create a server

