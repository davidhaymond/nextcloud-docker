# nextcloud-docker

My custom NextCloud setup featuring automatic HTTPS,
powered by Docker, PostgreSQL, Redis, and Caddy.

## Prerequisites

Install [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/).

## Usage

1. Clone the repo.
   ```sh
   git clone https://github.com/davidhaymond/nextcloud-docker.git
   cd nextcloud-docker
   ```
2. Copy `.env.example` to `.env` and adjust permissions:
   ```sh
   cp .env.example .env
   chmod 600 .env
   ```
3. Edit `.env` in your favorite editor, setting the environment variables appropriately.
   ```sh
   $EDITOR .env
   ```
4. Create a volume to store Caddy certificates and data:
   ```sh
   docker volume create caddy_data
   ```
4. Start the app:
   ```sh
   docker-compose up -d
   ```

## Upgrading

Upgrade to the latest version with:

```sh
git pull
docker-compose pull
docker-compose up -d
```
