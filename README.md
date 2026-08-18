# dashcamigo self-host

Run [dashcamigo](https://github.com/amkulikov/dashcamigo) on your own computer,
NAS, or home server with Docker Compose.

dashcamigo is a free, open-source dashcam viewer and editor. Recordings are
opened in your browser and are never uploaded to the container.

## Start

You need Docker with the Compose plugin.

```sh
git clone https://github.com/amkulikov/dashcamigo-self-host.git
cd dashcamigo-self-host
docker compose up -d
```

Open <http://localhost:8080>.

To use another port, copy `.env.example` to `.env` and change
`DASHCAMIGO_PORT` before starting the container.

## Update

```sh
docker compose pull
docker compose up -d
```

The container is stateless. There are no volumes, accounts, databases, or
application settings to back up. Browser settings remain in the browser.

## Stop

```sh
docker compose down
```

## HTTPS and remote access

Local use through `localhost` needs no additional setup. If you expose the app
to another device or the internet, put it behind HTTPS. Some browser features
are unavailable on an insecure remote connection.

See the upstream [self-hosting guide](https://github.com/amkulikov/dashcamigo/blob/main/docs/self-hosting.md)
for reverse-proxy examples, release verification, prebuilt archives, and
building from source.

## Upstream

This repository only contains the Docker Compose setup. The application source,
issues, releases, and documentation live in the main
[amkulikov/dashcamigo](https://github.com/amkulikov/dashcamigo) repository.

