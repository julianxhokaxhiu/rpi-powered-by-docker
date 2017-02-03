# rpi-powered-by-docker
Arch Linux ARM setup script to obtain a full RPI with Automatic Reverse Proxy without pain

## Stack
- IPv4/IPv6 support ( Dual Stack )
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/)
- [talmai/rpi-watchtower](https://hub.docker.com/r/talmai/rpi-watchtower) as the Docker auto-update manager
- [braingamer/nginx-proxy-arm](https://hub.docker.com/r/braingamer/nginx-proxy-arm/) as Reverse Proxy
- [hermanzdosilovic/rpi-docker-letsencrypt-nginx-proxy-companion](https://hub.docker.com/r/hermanzdosilovic/rpi-docker-letsencrypt-nginx-proxy-companion/) as automatic Let's Encrypt provisioner ( official companion docker for braingamer/nginx-proxy-arm )
- [apache-nginx-referral-spam-blacklist](https://github.com/Stevie-Ray/apache-nginx-referral-spam-blacklist) preloaded for every host

## Requirements
A clean Arch Linux ARM install with SSH capability as root user ( or any user which has sudo powers ).

## Installation
```bash
wget https://github.com/julianxhokaxhiu/rpi-powered-by-docker/archive/master.zip
unzip master.zip && cd rpi-powered-by-docker-master
find ./ -name "*.sh" -exec chmod +x {} \;
./install.sh
```

## Disclaimer
- The mapping of the domains to the Host IP is considered done already externally to this project ( through DNS Server or statically inside your `hosts` file )
