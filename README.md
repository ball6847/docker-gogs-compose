Docker Compose running gogs and postgresql

### Installation

```
docker-compose up -d
```

### Important

- My compose does not publish any http port, because I have my own nginx container running in front of this container, handle all incoming request then proxy to gogs on port 3000
- SSH port publishes at 22 port, just because I don't wanna caused more work to any user. Just use native ssh port. You need to set your openssh daemon to listen on other port to make it gogs works on port 22


### docker-compose-dev.yml

`docker-compose-dev.yml` is also available as alternative setup for development or testing purpose, which bind on port 10022 and 10080 for ssh and gogs itself.

```
docker-compose up -d -f docker-compose-dev.yml
```
