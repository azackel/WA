# Guest Book 📖 
[![](https://img.shields.io/badge/⋈%20Examples-Basics-green)](https://docs.near.org/tutorials/welcome)
[![](https://img.shields.io/badge/Gitpod-Ready-orange)](https://gitpod.io/#/https://github.com/near-examples/guest-book-js)
[![](https://img.shields.io/badge/Contract-js-yellow)](https://docs.near.org/develop/contracts/anatomy)
[![](https://img.shields.io/badge/Frontend-React-blue)](https://docs.near.org/develop/integrate/frontend)
[![Build Status](https://img.shields.io/endpoint.svg?url=https%3A%2F%2Factions-badge.atrox.dev%2Fnear-examples%2Fguest-book-js%2Fbadge&style=flat&label=Tests)](https://actions-badge.atrox.dev/near-examples/guest-book-js/goto)


The Guest Book is a simple app that stores messages from users, allowing to pay for a premium message.

![](https://docs.near.org/assets/images/guest-book-b305a87a35cbef2b632ebe289d44f7b2.png)


# What This Example Shows

1. How to receive $NEAR on a contract.
2. How to store and retrieve information from the blockchain.
3. How to use a `Vector`.
4. How to interact with a contract from `React JS`.

<br />

# Quickstart

Clone this repository locally or [**open it in gitpod**](https://gitpod.io/#/github.com/near-examples/guest_book-js). Then follow these steps:

### 1. Install Dependencies
```bash
npm install
```

### 2. Test the Contract
Deploy your contract in a sandbox and simulate interactions from users.

```bash
npm test
```

### 3. Deploy the Contract
Build the contract and deploy it in a testnet account
```bash
./deploy.sh
```

### 4. Get Messages

```bash
near view librovisitas.testnet get_messages '{"from_index":0, "limit":10}'
```

## 5. Add New Message

```bash
near call librovisitas.testnet add_message '{"text": "Primer mensaje"}' --accountId yairnava.testnet
```

```bash
near call owaguestbook.testnet add_message '{"text": "Primer mensaje premium"}' --amount 0.1 --accountId yairnava.testnet
```

## 6. Get Total Messages

```bash
near view guestbook1.testnet total_messages
```

---

# Learn More
1. Learn more about the contract through its [README](./contract/README.md).
2. Check [**our documentation**](https://docs.near.org/develop/welcome).