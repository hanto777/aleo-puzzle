# Puzzle Wallet on Aleo Protocol

## Install binaries

We are using docker to avoid dependencies incompatibility.

```bash
docker pull aleohq/snarkos:latest

docker run -it --rm aleohq/snarkos:latest /aleo/bin/snarkos
```

## Create a Puzzle Account

```bash
docker run -it --rm aleohq/snarkos:latest /aleo/bin/snarkos account new

  Private Key  xxxxxxxx-xxxxxxx-xxxxxxx
     View Key  xxxxxxxx-xxxxxxx-xxxxxxx
      Address  xxxxxxxx-xxxxxxx-xxxxxxx
```

## Deploy Contract

```bash
snarkos developer deploy --private-key <PRIVATE_KEY> --query <QUERY> --priority-fee <PRIORITY_FEE> <PROGRAM_ID>

docker exec -it cool_joliot bash -c "/aleo/bin/snarkos developer deploy --private-key <PRIVATE_KEY> --query 'https://testnet.puzzle.online' --priority-fee 0 puzzle_coinflip_0xawaz.aleo --broadcast 'https://testnet.puzzle.online/testnet/transaction/broadcast' --network 1"

curl https://testnet.puzzle.online/testnet/transaction/confirmed/at1qf7w8qg7nxkyyz3ecyer9jchz0p7axvl5gwsjjxr8tnuymc7zq8s774n9p
```
