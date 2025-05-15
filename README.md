# Requestrr

A lightweight request bot for Discord that allows users to request media (like movies and TV shows) via the chat interface.

> Originally forked and customized from the [Requestrr](https://github.com/darkalfx/requestrr) project. This version is tailored for simplified use and customization.

## Features

- 🎥 **Media Requesting** – Easily request Movies and TV Shows from Discord  
- 📡 **Service Integration** – Works with Radarr and Sonarr  
- 🔒 **Role-Based Access** – Only users with approved roles can make requests  
- ⚙️ **Simple Configuration** – Edit a JSON file to set everything up  
- 🐳 **Docker Support** – Containerized for easy deployment  

## Requirements

- A running instance of:
  - [Radarr](https://radarr.video/) (for movie requests)
  - [Sonarr](https://sonarr.tv/) (for TV show requests)
- A Discord bot token
- .NET Core SDK (if building locally)

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Rivwastaken/Requestrr.git
cd Requestrr
```

### 2. Configure the bot

Edit the `config.json` file and provide:

- Your **Discord Bot Token**
- **Radarr/Sonarr** API keys and base URLs
- **Role IDs** allowed to use the bot

### 3. Run the bot

#### Locally using .NET

```bash
dotnet run --project Requestrr/Requestrr.csproj
```

#### Using Docker

```bash
docker build -t requestrr .
docker run -d --name requestrr -v /path/to/config:/app/config requestrr
```

> Replace `/path/to/config` with the full path to your local `config.json` file.

## Available Commands

In Discord, users can type:

- `!movie <title>` – Search and request a movie  
- `!tv <title>` – Search and request a TV show  
- `!help` – Show available commands  

## Contributing

Pull requests are welcome!  
If you’ve added something cool, fixed a bug, or cleaned something up, feel free to submit a PR.

## License

MIT License  
Originally based on [darkalfx/requestrr](https://github.com/darkalfx/requestrr)

---

> *"No more spreadsheets. No more DMs. Just type and request."* 🎬
