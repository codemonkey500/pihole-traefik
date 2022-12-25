# Pi-hole using Traefik as a Reverse Proxy

## Setup

- Create docker network:
```bash
docker network create web
```

- Edit `.env` to configure environment variables

- Run:
```bash
docker-compose up -d
```

## Security

- This setup should be run on a Raspberry Pi in a home network
- Access to the system is only possible via Wireguard
- The exposed ports are bind to the wireguard ip range
- A traefik middleware ensures, that only the wireguard ip range can access the service

