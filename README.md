## Expected result

Listing containers must show three containers running and the port mapping as below:
```
$ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                  NAMES
d6752b317e6d   compose-dev-env_proxy                 "nginx -g 'daemon of…"   About a minute ago   Up About a minute   0.0.0.0:80->80/tcp, :::80->80/tcp   compose-dev-env_proxy_1
70bf9182ea52   compose-dev-env_backend               "/server"                About a minute ago   Up About a minute   8000/tcp                            compose-dev-env_backend_1
c67de604799d   mariadb                               "docker-entrypoint.s…"   About a minute ago   Up About a minute   3306/tcp                            compose-dev-env_db_1
```

After the application starts, navigate to `http://localhost:80` in your web browser or run:
```
$ curl localhost:80
["Blog post #0","Blog post #1","Blog post #2","Blog post #3","Blog post #4"]
```

Stop and remove the containers
```
$ docker-compose down
```

