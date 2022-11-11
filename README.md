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

## DNS Domaon name system

cs50.harvard.edu to IP addresses. DNS is generally provided by a server nearby, with a big table in its memory, of domain names and IP addresses.

Translate domain names to IP addresses

## HTTP, or Hypertext Transfer Protocol, 
standardizes how web browsers and web servers communicate within TCP/IP packets.

   HTTPS is the secure version of HTTP, ensuring that the contents of packets between the browser and server are encrypted.
