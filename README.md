# docker
### Ports are not available
```cmd
net stop winnat
docker start ... hoặc restart lại docker
net start winnat
```
### list port
```cmd
netstat -abno -p tcp
netstat -abno -p tcp | find "80"
```
### start/stop docker composer
```cmd
docker-compose up // start
docker-composer down // stop
```

setting POSTGRES_HOST to 127.0.0.1 or variants thereof? That means "localhost", which in a container means "the local container". Postgres isn't running inside the django container so that won't work.

Since you're using docker-compose, your containers are all running in a user-defined network. This means that Docker maintains a DNS server for you that maps service names to container ip addresses.

