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
