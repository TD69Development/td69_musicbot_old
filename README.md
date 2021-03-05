<a href="https://discord.GG/EjafVFUkFB"><img src="https://img.shields.io/discord/768016099421061183?color=7289da&logo=discord&logoColor=white" alt="Discord server" /></a>

## Usage

**Requires [Node.js](https://nodejs.org) version v14.x or above.**

1. Install [Node.js](https://nodejs.org) and [Yarn (Optional)](https://yarnpkg.com)
2. Delete old `.env`, rename `.env.schema` to `.env` and fill out the values (example on .env.example)
3. Install dependencies as stated [here](https://github.com/zhycorp/disc-11#Installation) before you continue surfing
4. Run `npm run build`, or `yarn run build` if you're using Yarn package manager
5. Optional thing, prune dev dependencies (this is good to save disk spaces):
```shell script
$ npm prune --production
# or with yarn
$ yarn install --production
```
6. Start it with `npm start` or `yarn start`, and you're done!

Notes: 
1. You only need to configure .env file when you're using the [Docker image](https://github.com/zhycorp/disc-11#Docker)
2. If you're using "Deploy to Heroku" button, you don't need to do this.

## Installation

Without optional packages
```shell script
$ npm install --no-optional
# or with yarn
$ yarn install --ignore-optional
```

With optional packages (recommended)

```shell script
$ npm install
# or with yarn
$ yarn install
```

### Volumes
[Docker Volumes](https://docs.docker.com/storage/volumes/) are needed to store cache and logs persistently.

### Example:
```shell
$ docker run --env-file .env --volume cache:/app/cache --volume logs:/app/logs --restart unless-stopped hazmi35/jukebox
```
We also provide [docker-compose.yml](docker-compose.yml) if you want to go that way.

### Compose Example
```
$ docker-compose up
```

## Features
- A production-ready music bot, suitable for you that don't like to hassling with the code
- Basic Commands (Help, Ping, Invite & Eval [for advanced bot owners])
- Basic Music Commands (Play, Skip, Stop, Pause & Resume, Now Playing, Queue, Repeat, Volume)
- Caching (cache youtube downloads)
- Configurable (easy to use)
- Docker-friendly (if you're advanced user)
- Lightweight (only around 120MB with dev dependencies pruned)