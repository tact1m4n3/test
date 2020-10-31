# Dynamic Server

## Why use this library?
- It's an interface that helps you communicate with your website
- You can use it as a webserver
- Verry easy to customize requests and responses
- It's really easy to use

## How to?
- First, import this library and initialize your server...
```
'''
Make sure you have this library copied in your folder
Download it from this repository
'''
from dynamic_server import * 

server = Server("localhost", 77666) # ip and port number
```
- Then create some functions to handle requests
```
# it takes as arguments a request and a response
def say_hello(req, res):
    res.body = "Hello"
```
- After that, use the server's methods get and post to map an address to your function(get and post are types of requests)
```
server.get("/hello", say_hello)
```
- Finnaly, call the run method
```
server.run()
```
