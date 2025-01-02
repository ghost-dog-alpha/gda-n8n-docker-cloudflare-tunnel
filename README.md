# gda-n8n-docker-cloudflare

The purpose of this configuration is to rapidly enable a n8n instance on a local network isolated server to have HTTPS certificates issued via Cloudflare.


Get up and running with n8n on the following platforms:

* [DigitalOcean tutorial](https://docs.n8n.io/hosting/server-setups/digital-ocean/)
* [Hetzner Cloud tutorial](https://docs.n8n.io/hosting/server-setups/hetzner/)

If you have questions after trying the tutorials, check out the [forums](https://community.n8n.io/).

## PCommands to build and run the containers

### Build te caddy container
```sudo docker build -t caddy .```

### Compose the containers
```sudo docker-compose up -d```

### Debug the containers

Look at the logs
```sudo docker logs n8n-docker-caddy-caddy-1```

Look at the env
```sudo docker exec -it n8n-docker-caddy-caddy-1 env```

List modeules
```sudo docker run --rm caddy caddy list-modules | grep dns.providers.cloudflare```