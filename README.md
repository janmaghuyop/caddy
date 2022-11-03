Caddy
=====
Caddy playground.

Links:
- https://hub.docker.com/_/caddy

Usage:
```bash
cd caddy

# mkcert
mkcert -install
mkdir tmp && cd tmp && mkcert localhost localhost 127.0.0.1

podman-compose pull
podman-compose up -d
podman-compose ps

# caddy
curl https://localhost:8443
curl https://localhost:8443/whoami

# whoami
curl localhost:8081
```

TODO:
- whitelist 
