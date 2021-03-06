# NASA Mars Explorer

[ ![Codeship Status for marceldiass/mars](https://codeship.com/projects/fcbdd4b0-97bc-0133-de51-66b8883e9f8d/status?branch=master)](https://codeship.com/projects/125899)

Rest service to receive commands

## Compile

Use Maven 3 to compile this project

## Deploy

There is a jboss-web.xml file mapping the context root to /

So if you deploy in a wildfly the path will be /rest/mars

## Docker Image

docker run -d -p 8080:8080 marceldiass/mars

## Consume

The end point accept HTTP POST method and the path is /rest/mars/{actions}

You can test it with curl.
Example:
```bash
curl -i -X POST "http://localhost:8080/rest/mars/MML"

HTTP/1.1 200 OK
Connection: keep-alive
X-Powered-By: Undertow/1
Server: WildFly/9
Content-Type: text/plain
Content-Length: 9
Date: Thu, 07 Jan 2016 21:59:31 GMT

(0, 2, W)

```
