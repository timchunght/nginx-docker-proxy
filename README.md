# nginx-docker-proxy
docker sock NGINX reverse proxy configuration with basic auth

The Goal is to be able to attach to docker remotely via the REST API in a secure manner. 

In this example, we will use nginx to act as the reverse proxy for the docker unix socket. 

A special version of modified nginx is require and can be found here
```
https://github.com/timchunght/nginx/tree/docker-socket
```

We will then use the ``host:<port_exposed_by_nginx>/path/for/docker_attach_rest_api_and/container_id`` as input to the command line client.

This is similar to how Heroku works actually whe you do ``heroku run``.
