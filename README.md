# cloudflare-railgun
Dockerfile for cloudflare's railgun

cloudflare-railgun 5.0.2

docker run --name railgun-memcached -d --restart=always memcached

docker run -d --restart=always --name railgun -p 2408:2408 --link railgun-memcached:memcached -e RG_ACT_TOKEN= -e RG_ACT_HOST= -e RG_LOG_LEVEL=1 rungeict/cloudflare-railgun

Also see dockercloud.yml
