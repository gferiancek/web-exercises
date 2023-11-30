# Part 1

## What is HTTP?
HTTP (Hypertext Transfer Protocol) is a standard for communicating between a client and a server. (Requests/Responses)

## What is a URL?
A URL is a type of URI that points to a specific resource on the web, such as a web page, an image, etc.

## What is DNS
DNS (Domain Name System) is like the phone book of the web. It takes our human readable Hostnames and maps them to their IP Address.

## What is a query string?
A query string is a part of a URL that allows you to pass extra information to the webpage you're viewing. (`? key1=value&key2=value`)

## What are two HTTP verbs and how are they different?
The two most common are GET and POST.

GET simply gets info from the server without any side effects, while POST is intended to save/change data that is on the server.

## What is an HTTP Request?
A Request is made by a client to get/post/etc something to/from the server.

## What is an HTTP Response?
A Response is sent from the server to the client after it makes a request.

## What is an HTTP Header? Give a couple examples.
HTTP Headers are attached to requests/responses and contains data about them.

For requests, some examples are an API Key, Accept (text/html, application/json, etc) and Accept-Language.

For responses, some examples are the Status Code and the Last Modified date.

## What are the processes that happen when you type `http://somesite.com/som/page.html` into a browser?
- The browser needs to turn the hostname into an IP Address, and does this with the help of DNS.
  - It starts by checking locally for a cached DNS lookup, and then will move on to check your router, your ISP, and eventually a DNS Server.
- The browser then makes a request to that IP Address for a specific page/queries.
- The server often has some kind of backend work it does to formulate a response.
  - This could be finding the page of the day on Wikipedia and building the HTML, pulling data about a specific user for a Profile page, etc.
- The server, whether it failed or succeed, then sends a response back the browser.
- The browser then makes the DOM for the webpage.
- Any additional files (css/js) and resources (images, videos, etc) are all made in separate calls!

# Part 2

## Using curl, make a GET request to icanhazdadjoke API for all injokes involving the word 'pirate'.
```
curl https://icanhazdadjoke.com/search?term=pirate
// What did the pirate say on his 80th birthday? Aye Matey!
// Why couldn't the kid see the pirate movie? Because it was rated arrr!
// What does a pirate pay for his corn? A buccaneer!
// Why do pirates not know the alphabet? They always get stuck at "C".
// Why are pirates called pirates? Because they arrr!
```

## Use dig to find the IP Address of icanhazdadjoke.com
```
dig https://icanhazdadjoke.com // 172.18.48.1
```