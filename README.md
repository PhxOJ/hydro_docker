# This is a way to install hydro via docker

Hydro Official Repo [https://github.com/hydro-dev/Hydro](https://github.com/hydro-dev/Hydro)

## Prerequisite

- docker
- docker-compose (you can just use docker plugin)
- Git

## Build image manually

```bash
docker pull ubuntu:22.04
docker run --privileged -it --name phx-oj ubuntu:22.04
```

Now you have entered into container

```bash
export USER=root
apt-get update
apt-get install -y curl
apt-get install -y git cron vim (you can adjust here)
LANG=zh . <(curl https://hydro.ac/setup.sh)
```

Exit container

```
docker stop phx-oj
docker commit phx-oj phxoj:latest
```

## Use docker compose to start

First you should clone this git repo and enter in it.

```
docker compose up -d
```
