# Distribrewed stack
This repo contains docker-compose files to start the distribrewed stack.

### Requirements
To start the stack you have to install [docker](https://docs.docker.com/engine/installation/) and [docker-compose](https://docs.docker.com/compose/install/).

### Default port mapping

Program | Port
 --- | ---
Distribrewed | 8000
Grafana | 3000
Prometheus | 9090
Consul | 8500
RabbitMQ | 5672
RabbitMQ UI | 8100


### Starting the stack

```bash
docker-compse up -d
```

### Upgrading the stack
```bash
docker-compose down
docker-compose pull
docker-compose up -d
```

### Deleting all data
```bash
sudo rm -r data
```

### Changing default passwords

Edit `.env` file to change default passwords.

### Starting the telegram worker

Edit `./telegram/.env` and set telegram token and chat id.

```bash
cd telegram
docker-compose up -d
```