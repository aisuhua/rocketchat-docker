# RocketChat

- https://github.com/RocketChat/Docker.Official.Image
- [Configuring SSL Reverse Proxy](https://docs.rocket.chat/deploy/rocket.chat-environment-configuration/configuring-ssl-reverse-proxy)

## Backup and Restore

直接拷贝 volume

```sh
vackup export rocketchat-docker_mongodb_data rocketchat-docker_mongodb_data.tar.gz
vackup import rocketchat-docker_mongodb_data.tar.gz rocketchat-docker_mongodb_data
```

备份数据库

```sh
# 备份
docker exec rocketchat-docker-mongodb-1 sh -c 'mongodump --archive' > db.dump

# 恢复  
docker-compose up mongodb
docker exec -i rocketchat-docker-mongodb-1 sh -c 'mongorestore --archive' < db.dump
```

