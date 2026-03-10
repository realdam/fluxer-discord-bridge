## Creating your bots

1. Follow [this guide](https://discordjs.guide/legacy/preparations/app-setup) to set up your Discord bot. Make a note of the token, you'll need it in a minute.
2. Set up your bot on Fluxer by going to User Settings > Applications and follow the instructions there. Again, make note of your token. Don't get them mixed up.
3. Use the OAuth builders to invite your bots to their respective servers. Both bots require the Manage Roles, Manage Webhooks, Send Messages, and Read Message History permissions.

## Installation with Docker (RECOMMENDED)

Docker Desktop is not required. A normal Docker Engine install with the Compose plugin works on headless Linux servers, including Fedora.

### Setup

1. Install Docker Engine and the Compose plugin on the host.
2. Clone or extract this repository.
3. From the repo root, copy `Bot/example.env` to `.env`, then fill in your Fluxer and Discord bot tokens.
4. Create a writable data directory with `mkdir -p db`.
5. Copy `docker-compose.example.yml` to `docker-compose.yml` if you want to keep local edits out of git.

### Testing

To build and start your bot from the repo root, run `docker compose up -d --build`.  
To stop it, run `docker compose down`.  
Check that your bot is working by typing `brdg;help` (or use your custom prefix if you set one). If you need to troubleshoot, run `docker compose logs -f fluxer-discord-bridge`.

## Installation from source (NodeJS)

### Setup

1. Download and install NodeJS from [their website](https://nodejs.org/en/download).
2. Download and extract the most recent source code from the [Releases page](https://github.com/rillabel/fluxer-discord-bridge/releases). Note the path to your folder.
3. Copy `Bot/example.env` to `.env`. Fill in `.env` with your Fluxer and Discord bot tokens. Feel free to set a custom command prefix while you're here.

### Testing

To start your bot, open your command line and run `cd {PATH_TO_YOUR_BOT_FOLDER} && node --env-file=.env Bot/Bot.js`.  
To stop it, close your command terminal.  
Check that your bot is working by typing `brdg;help` (or use your custom prefix if you set one).  
