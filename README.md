# Who Said Innopolis

This repository contains the Docker Compose file for running the Who Said Innopolis bot and server.

## Prerequisites

Before running the services, make sure you have the following installed:
- Docker
- Docker Compose

## Getting Started

To get started, follow the steps below:

1. Clone this repository to your local machine.
2. Navigate to the repository's directory.

## Configuration

The services in this Docker Compose file require environment variables to be set. Create two separate .env files: .env.bot and .env.server. These files should contain the necessary environment variables for the bot and server services, respectively. Use the *.template files as an example.

## Usage

To start the services, run the following command:

```bash
docker-compose up -d
```

This command will build the necessary Docker images and start the containers in detached mode.

To stop the services, run the following command:

```bash
docker-compose down
```

## Services

This Docker Compose file defines two services:

- Bot
  - Image: salloum/who-said-innopolis-bot
  - Build context: ./who-said-innopolis-bot
  - Environment variables: Loaded from .env.bot file
  - Restart policy: Always
- Server
  - Image: salloum/who-said-innopolis-server
  - Build context: ./who-said-innopolis-server
  - Environment variables: Loaded from .env.server file
  - Ports: Exposed port 5000 on the host machine, mapped to port 5000 in the container
  - Restart policy: Always
  
## Contributing

If you would like to contribute to this project, feel free to submit a pull request. Please ensure that your changes align with the project's coding standards and conventions.

## License

This project is licensed under the MIT License.
