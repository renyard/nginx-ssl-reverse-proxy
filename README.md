## Nginx proxy server in a box.

This Docker container is forked from https://github.com/paimpozhil/nginx-ssl-reverse-proxy
and modified to provide the best security to support the backend of the Validity Chrome extension.

** This is only intented to provide enough support for the latest version of Chrome & Opera. **

## How to run :

```
$ git clone https://github.com/renyard/nginx-ssl-reverse-proxy.git
$ cd nginx-ssl-reverse-proxy
```
Add the server.crt and server.key certificates to the nginx-ssl-reverse-proxy/certs/ directory.
```
$ docker build -t nginxsslproxy .
$ docker run -d -p 443:443 --link [container name of your actual webserver]:site nginxsslproxy
```

Credits :

Based on:
- https://github.com/paimpozhil/nginx-ssl-reverse-proxy
- https://github.com/dhrp/docker-nginx-proxy
