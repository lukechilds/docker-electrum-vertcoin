
# docker-electrum-vertcoin

> Run a Vertcoin Electrum server with one command

A Docker configuration with sane defaults for running a full Vertcoin node behind an ElectrumX server.

## Usage

```
docker-compose up
```

This will pull the latest version of vertcoind and ElectrumX, start syncing the blockchain, generate an SSL certificate and start listening for secure Electrum traffic on port 55002.

All blockchain/vertcoind data will be stored in ./data/vertcoind and all ElectrumX data will be stored in ./data/electrumx. This is stored on the host machine and mounted on the docker containers as a volume, meaning it will persist across reboots/updates/containers etc.

## License

MIT © Luke Childs
