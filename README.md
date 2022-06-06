# Consul datacenter config for my-epoch project

## Getting Started

### Generating certificates

1. Go to cert directory, create CA and certificate files by running

```console
cd cert
consul tls ca create
consul tls cert create -server
```

2. Create copies of `.example.json` files in `config` directory

```console
cp config/consul-client.example.json config/consul-client.json
cp config/consul-client.example.json config/consul-client.json
```

3. By running `consul keygen` generate gossip encryption key and replace `YOUR_ENCRYPTION_KEY_HERE` by your key
   in `config/consul-client.json` and `config/consul-client.json`

## Running

In the root directory run

```console 
docker compose up
```

and it's all

## Additional information

* Consul documentation https://www.consul.io/docs