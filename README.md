# Creating an NFT collection in the TON main network

## Preparation.

1) Create a new wallet (for example, in [Tonkeeper](https://tonkeeper.com/) or https://wallet.ton.org).

   This wallet will manage the collection.

   Only by using this wallet you'll be able to create new NFT tokens for this collection or change the collection's metadata

2) When creating a wallet be sure to write down 24 English words for recovery.

   Be sure to save them in a safe place.
 
   If you lose them, you will permanently lose access to your wallet and collection management.

   No one but you should know your secret words.


3) Add the TON tokens to your wallet.

   You need about ~0.07 TON to create one NFT (for example, if you want to create 1000 NFT, you need about 70 TON).


## Script

This repository contains an open-source script in javascript to deploy the NFT collection.

The [script.md](https://github.com/tondiamonds/ton-nft-deployer/blob/main/script.md) describes how to run it.

The parameters of the .env are the same as those of the web page, so you can see the description of the parameters in the previous paragraph.


## Check

* Open your wallet address at https://tonscan.org

* You will see outgoing transactions from your wallet to your collection address.

* Open https://tonscan.org/nft/<address_your_collection>. Verify that the displayed data is correct.

* You will see outgoing transactions from your collection - NFT deployments.

* Open https://tonscan.org/nft/<nft_address>. Check that the displayed data is correct.


## NFT Deploy Basics

Your smart contracts must be compatible with the [NFT standard](https://github.com/ton-blockchain/TIPs/issues/62).

The contracts can be found at https://github.com/ton-blockchain/token-contract/tree/main/nft

`nft-collection-editable.fc` for a collection and `nft-item.fc` for a collection item.

The JavaScript SDK [TonWeb](https://github.com/toncenter/tonweb) version 0.0.38 and above (version is important) also uses these smart contracts.

The web page and script above use TonWeb.
