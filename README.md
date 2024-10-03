<h2 align=center>Register a NFT as an IP asset on Story Protocol</h2>

## Info

-   This script will create a NFT on Story Protocol and then will register that NFT as an IP asset on Story Protcol
-   You can even register Iliad Commemorative NFT or Color NFT as an IP asset on Iliad Testnet
-   Currently only NFTs on Story Protocol are supported to register as an IP asset, in future they will enable function to register others' chain NFT as an IP asset on Story Protocol

## Prerequisites

-   Need to have $IP faucet, you can get all the faucet site links from [Story Protocol Docs](https://docs.story.foundation/docs/faucet)
-   Need to have Linux Based Terminal like [Codespace](https://github.com/codespaces) , [Gitpod](https://gitpod.io) , VPS or WSL
-   Pinata JWT token, To get Pinata JWT token, Visit : [Pinata Website](https://pinata.cloud/) , Click on `Get Started` and register using an email address and then follow all the steps mentioned below on the img

![Img1](https://github.com/user-attachments/assets/78878ba8-b8f0-4dff-a133-f9436100e0b1)

## Installation

-   Clone this Repo

```bash
git clone https://github.com/0xAJPanda/Story-Protocol-NFT-IP-Asset.git && cd Story-Protocol-NFT-IP-Asset
```

-   Install dependencies

```bash
npm install
```

-   Set .env file , Replace Wallet with your private and and JWT with Pinta JWT (alternatively you can rename .env.example to .env and fill in the info )

```bash
cat <<EOF > .env
WALLET_PRIVATE_KEY=$WALLET
PINATA_JWT=$JWT
EOF

```

-   Create SPG collection, this will create the NFT collection and return the contract address you can make changes to it if you wish on the scripts/utils/createSpgNftCollection.ts

```bash
npm run create-spg-collection
```

-   Copy the Nft contact address and add it to the .env file using the command below or simply do with the editor

```bash
echo "NFT_CONTRACT_ADDRESS=$CONTRACT" >> .env
```

-   Deploy the NFT to the network this should return the url in the explorer, you can change values in the scripts/metadataExample.ts as you wish.

```

npm run metadata

```

-   Congratulation you made it!!!
