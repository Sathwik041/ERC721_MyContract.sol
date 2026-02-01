# SAT_TOKEN — ERC721 NFT Smart Contract

SAT_TOKEN is a secure and minimal **ERC721 Non-Fungible Token (NFT) smart contract** built using **OpenZeppelin Contracts v5.5.0** and deployed on the **Monad Testnet**. The contract follows industry best practices for NFT creation, ownership control, and metadata management.

---

## Overview

* **Token Standard:** ERC721
* **Token Name:** SAT_TOKEN
* **Symbol:** SAT
* **Blockchain Network:** Monad Testnet
* **Smart Contract Library:** OpenZeppelin
* **Access Control:** Owner-based (Ownable)

This contract enables the contract owner to mint NFTs safely and assign metadata URIs compliant with NFT marketplace standards.

---

## Key Features

* ERC721 compliant NFT implementation
* Built using OpenZeppelin’s audited contracts
* Owner-restricted minting for security
* Supports token metadata via `tokenURI`
* Safe NFT minting using `_safeMint`
* Compatible with NFT explorers and marketplaces

---

## Access Control Model

The contract uses **OpenZeppelin’s `Ownable` pattern**:

* Only the contract owner can mint NFTs
* Prevents unauthorized token creation
* Simple and effective permission management

This design mirrors common real-world NFT collections where the creator retains minting rights.

---

## Smart Contract Functions

### Minting NFTs

```solidity
function safeMint(address to, uint256 tokenId, string memory uri)
    public
    onlyOwner
```

* Mints a new NFT to the specified address
* Assigns a metadata URI (IPFS or HTTPS)
* Restricted to the contract owner

---

## Metadata Standard

Each NFT uses a standard metadata JSON format:

```json
{
  "name": "SAT NFT #1",
  "description": "A unique NFT minted on Monad Testnet",
  "image": "ipfs://<IMAGE_CID>",
  "attributes": [
    { "trait_type": "Creator", "value": "Sathwik" },
    { "trait_type": "Network", "value": "Monad Testnet" }
  ]
}
```

---

## Deployment Details

* **Smart Contract Address:**
  `0xec4ceC7061B1135CB66dC93cAcAbf6034Faed9CE`

* **Monad Testnet Explorer:**
  [https://testnet.monadvision.com/token/0xec4ceC7061B1135CB66dC93cAcAbf6034Faed9CE](https://testnet.monadvision.com/token/0xec4ceC7061B1135CB66dC93cAcAbf6034Faed9CE)

---

## How to Use

1. Deploy the contract with your wallet address as the initial owner
2. Call `safeMint` with a unique `tokenId` and metadata URI
3. View minted NFTs on the Monad explorer or supported NFT platforms

---

## Use Cases

* NFT collections
* Portfolio or academic blockchain projects
* Monad ecosystem demos
* Learning ERC721 and OpenZeppelin standards

---

## License

This project is licensed under the **MIT License**.

---
