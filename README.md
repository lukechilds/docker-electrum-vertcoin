
# docker-electrum-vertcoin

> Run a Vertcoin Electrum server with one command

A Docker configuration with sane defaults for running a full Vertcoin node behind an ElectrumX server.

## Usage

```
docker-compose up
```

This will pull the latest version of vertcoind and ElectrumX, start syncing the blockchain, generate an SSL certificate and start listening for secure Electrum traffic on port 55002.

All blockchain/vertcoind data will be stored in ./data/vertcoind and all ElectrumX data will be stored in ./data/electrumx. This is stored on the host machine and mounted on the docker containers as a volume, meaning it will persist across reboots/updates/containers etc.

### Is this secure?

Yep, this is built to have sensible, safe defaults out of the box. vertcoind JSON-RPC is only accessible from the ElectrumX container, it's never exposed to the internet, it's not even exposed to localhost. ElectrumX will generate a fresh SSL certificate on first boot and only listen for SSL traffic. Unencrypted traffic will be ignored.

## License

MIT © Luke Childs
