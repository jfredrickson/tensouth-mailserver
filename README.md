# mailserver

Based on [Docker Mailserver](https://github.com/docker-mailserver/docker-mailserver).

## Setup

Override `mailserver.env` variables in `.env`.

## Updating

In addition to `docker-compose pull`, also get the tools:

```
DMS_GITHUB_URL='https://raw.githubusercontent.com/docker-mailserver/docker-mailserver/master'
wget "${DMS_GITHUB_URL}/mailserver.env"
wget "${DMS_GITHUB_URL}/setup.sh"
chmod a+x ./setup.sh
```

Also fetch and compare the latest `docker-compose.yml`:

```
wget "${DMS_GITHUB_URL}/docker-compose.yml"
```

## Important notes

Instead of `docker-compose start` or `docker-compose stop`, use `docker-compose down` and `docker-compose up` per DMS instructions.
