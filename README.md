# RocketChat

- https://github.com/RocketChat/Docker.Official.Image
- [Configuring SSL Reverse Proxy](https://docs.rocket.chat/deploy/rocket.chat-environment-configuration/configuring-ssl-reverse-proxy)

## Backup and Restore

```sh
vackup export rocketchat-docker_mongodb_data rocketchat-docker_mongodb_data.tar.gz
vackup import rocketchat-docker_mongodb_data.tar.gz rocketchat-docker_mongodb_data
```
