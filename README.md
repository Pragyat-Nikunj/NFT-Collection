# NFT Collection (Foundry)

A professional NFT collection project built with [Foundry](https://book.getfoundry.sh/), featuring two smart contracts:

- **BasicNft**: Standard ERC721 NFT with custom token URIs.
- **MoodNft**: Dynamic ERC721 NFT that visually reflects the owner's mood (happy/sad) using on-chain SVG images.

---

## Deployed Contracts

- **MoodNft (Sepolia)**:  
  [`0x8b2B0aF0AA72D7CF7650C7f9f0b99cF0B0aFD19B`](https://sepolia.etherscan.io/address/0x8b2B0aF0AA72D7CF7650C7f9f0b99cF0B0aFD19B)

---

## Features

- **Modern Solidity**: Written in Solidity ^0.8.18.
- **On-chain Metadata**: SVG images encoded and stored on-chain.
- **Automated Scripts**: Deploy, mint, and interact using Foundry scripts.
- **Comprehensive Testing**: Unit tests for contract logic.

---

## Directory Structure

```
src/        # Smart contracts
script/     # Deployment & interaction scripts
test/       # Unit tests
img/        # SVG images for MoodNft
lib/        # External dependencies
```

---

## Getting Started

### Prerequisites

- [Foundry](https://book.getfoundry.sh/getting-started/installation)
- Node.js (for some tooling)
- Git

### Installation

```bash
git clone <repo-url>
cd nft-collection
forge install
```

### Add SVG Images

Place your `sad.svg` and `happy.svg` files in the `img/` directory. These will be encoded and used by the MoodNft contract.

---

## Usage

### Local Development

Start a local node:
```bash
make anvil
```

### Deploy Contracts

Deploy BasicNft:
```bash
make deploy
```

Deploy MoodNft:
```bash
make deployMoodNft
```

### Mint NFTs

Mint a BasicNft:
```bash
make interact
```

Mint a MoodNft:
```bash
make mintMoodNft
```

### Flip Mood

Use the `FlipMoodNft` script to change the mood of a MoodNft token.

---

## Testing

Run all unit tests:
```bash
make test
```

---

## License

MIT