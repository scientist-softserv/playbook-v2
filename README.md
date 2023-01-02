# Local Development

Any changes made to client files and server files will need a server restart. You can also force a restart with CTRL+C until the process exits. Then followed by `docker compose up`

## Prerequisites

* Docker + Docker Compose (via [Docker Desktop](https://www.docker.com/products/docker-desktop/))
* Linux / macOS / Windows 10-11 Pro or Enterprise

## Running the project
1. Clone the project from [Playbook-v2](https://scientist-softserv/playbook-v2).
2. Run the following commands:
```bash
docker compose up
docker compose exec web sh
yarn   # only necessary the first time
```

## Stopping the project
1. Hit Ctrl+C
2. Run `docker-compose stop`

## Removing the containers
```
docker compose down
```
To wipe the database as well, use
```
docker compose down --volumes
```

# Note

## Building production assets

Once you're ready to deploy your changes, you need to build the client assets into a production optimized bundle:

```bash
yarn build
```

# Helm Deplyment

Our deployments are helm based and setup through github actions.