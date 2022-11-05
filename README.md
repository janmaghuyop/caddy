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
mkdir tmp && cd tmp && mkcert caddy localhost 127.0.0.1
cp $(mkcert -CAROOT)/rootCA.pem tmp

podman-compose pull
podman-compose up -d
podman-compose ps

# caddy
curl https://localhost:8443
curl https://localhost:8443/whoami

# whoami
curl localhost:8081

# test on alpine
podman-compose exec alpine sh
telnet caddy 8080
curl -Lv curl --cacert rootCA.pem http://caddy:8080
curl -Lv curl --cacert rootCA.pem http://caddy:8080/whoami
```

TODO:
- whitelist 
