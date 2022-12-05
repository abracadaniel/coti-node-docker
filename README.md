# COTI Testnet Node in Docker with Nginx and LetsEncrypt Certificate
This will only run a testnet node. To run a mainnet node, your testnet node will first have to be approved by the COTI team.

## How to run
First you will need a domain pointing to the server you will run the node on.
Then update the variables saying <CHANGE> in the following files
1. docker-compose.yml
2. data/coti-fullnode/fullnode1.properties: server.ip
3. data/nginx/server.conf

To run the node, run docker compose using the docker-compose.yml file.

## Obtaining credentials
To obtain the credentials global.private.key and fullnode.seed needed in fullnode1.properties, you will have to sign up for a wallet on the [COTI Viper Wallet](https://pay.coti.io/).

## Repositories
This docker compose yml file is based on the official [coti/coti-node](https://github.com/coti-io/coti-node) repo, and the container for running nginx and automatic SSL certificate renewal is using the [jonasal/nginx-certbot](https://github.com/JonasAlfredsson/docker-nginx-certbot) repo.