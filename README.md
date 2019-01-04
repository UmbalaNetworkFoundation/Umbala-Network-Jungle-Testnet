# UmbalaNetowork-Testnet

Welcome to the Umbala Netowork - Testnet

## Dependencies

- [Docker](https://docs.docker.com) Docker 17.05 or higher is required
- [docker-compose](https://docs.docker.com/compose/) version >= 1.10.0

## Clone project

```
git clone git@github.com:UmbalaNetworkFoundation/Umbala-Network-Jungle-Testnet.git
cd fullnode
```

## Setup a fullnode in 5 seconds using the shell

```
./run.sh
```

## Setup a fullnode manually in 1 minute

The first step, create the desired directory:

```
mkdir -p /data/eos/nodeos-data-volume/nodeos-data-umb/data
```

The second step is to prepare the configuration file:

```
cp -r config /data/eos/nodeos-data-volume/nodeos-data-umb
```

The third step, join the network:

```
docker-compose -f docker-compose-umb-init.yaml up -d
```

## Stop/Restart syncing

To stop:

```
docker-compose -f docker-compose-umb.yaml down
```

To restart:

```
docker-compose -f docker-compose-umb.yaml down
docker-compose -f docker-compose-umb.yaml up -d
```
## Chain info

```
{
  "chain_id": "5fff1dae8dc8e2fc4d5b23b2c7665c97f9e9d8edf2b6485a86ba311c25639191"
}
```

## P2P LIST

```

```

## HTTP API LIST

API nodes:
```
http://tracker.umba.la/v1/chain/get_info
```

## Faucet

Creating accounts on umbala network testnet is pretty simple:

#### Free Account
Create account using: http://faucet.umbala.network/create_account?new_account_name

Example:
```
curl http://faucet.umbala.network/create_account\?111111111ooo
```


#### Get Free tokens
Get free token with: http://faucet.umbala.network/get_token?your_account_name.   

You can get 1000 tokens each call and max 10000 tokens per day.  

Example:
``` 
curl http://faucet.umbala.network/get_token?111111111ooo
```