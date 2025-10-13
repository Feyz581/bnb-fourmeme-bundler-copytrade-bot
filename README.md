# 🦾 Four.meme & PancakeSwap Trading Bot

**Atomic Bundler | Copy Trade | Snipe Graduated Tokens | Liquidity Automation**

<div align="center">

A professional-grade automated trading suite for **BNB Smart Chain**, featuring **Four.meme token sniping**, **copy-trading**, and **bloXroute atomic bundling** for **MEV-protected execution**.

[![Hardhat](https://img.shields.io/badge/Built%20with-Hardhat-yellow.svg)](https://hardhat.org/)
[![Solidity](https://img.shields.io/badge/Solidity-0.8.19-blue.svg)](https://soliditylang.org/)
[![BSC](https://img.shields.io/badge/BNB%20Chain-Compatible-green.svg)](https://www.bnbchain.org/)
[![bloXroute](https://img.shields.io/badge/MEV%20Protection-bloXroute-orange.svg)](https://bloxroute.com/)
[![License: ISC](https://img.shields.io/badge/License-ISC-lightgrey.svg)](./LICENSE)

</div>

![img-banner](https://i.imgur.com/GRJ6HHa.png)
---

## ⚙️ Overview

This repository provides a **next-generation trading infrastructure** for **BNB Smart Chain**, combining automation, efficiency, and protection.
It supports **sniping, bundling, copy-trading, and graduated token strategies** on both **Four.meme** and **PancakeSwap V3**.

Built for **speed**, **atomicity**, and **precision**, it enables:

* Instant token launches and liquidity provisioning
* Safe and simultaneous operations via **bloXroute atomic bundles**
* Copying of top trader strategies in real-time
* MEV-safe transaction flow with gas optimization

---

## 🚀 Key Features

| Category                         | Description                                                                                 |
| -------------------------------- | ------------------------------------------------------------------------------------------- |
| **🪙 Token Deployment**          | One-click ERC20 deployment with full control over name, symbol, and supply                  |
| **💧 Liquidity Management**      | Automatic pool creation, initialization, and liquidity provisioning on PancakeSwap V3       |
| **⚡ Atomic Bundling**            | MEV-protected multi-transaction bundling through bloXroute                                  |
| **🎯 Sniping Engine**            | High-speed sniping on **Four.meme** for newly deployed or graduated tokens                  |
| **🔁 Copy Trading**              | Mirrors successful traders’ buy/sell operations automatically                               |
| **📊 Graduated Token Detection** | Identifies and snipes tokens after migration or pool graduation                             |
| **📦 Bundle Executor**           | Executes token creation, pool setup, and liquidity injection in a single atomic transaction |
| **🛡 Security**                  | OpenZeppelin contracts, MEV protection, and transaction validation                          |
| **🧪 Simulation**                | Fork BSC mainnet locally with Hardhat for pre-deployment testing                            |
| **📈 Volume Bot (Optional)**     | Generates smart buy/sell volume to increase market activity                                 |

---


## ⚙️ Configuration

Create a `.env` file in the project root:

```env
# --- Authentication ---
AUTHORIZATION_HEADER=MjIyNGRlYjItMWUxYy00YWY2LTgzNTEtZDFmMTc5NDk3ZjA4OjczZjczNDU1YjgwNmE3MTRhMzBjOWVkY2NmMjIyNjMx
PRIVATE_KEY=your_private_key
BLOXROUTE_ENDPOINT=https://api.blxrbdn.com
RPC_ENDPOINT=https://winter-wild-isle.bsc.quiknode.pro/f31cb3e6e45fdd573a825c77b5ea62d2de9cd884/

# --- TOKEN CONFIGURATION ---
TOKEN_NAME=MyToken
TOKEN_SYMBOL=MTK
TOKEN_SUPPLY=1000000

# --- TRADING CONFIGURATION ---
GAS_PRICE_MULTIPLIER=1.2
FUTURE_BLOCK_OFFSET=5
SNIPE_GRADUATED=true

# --- POOL CONFIGURATION ---
FEE_TIER=3000
INITIAL_PRICE=1

```

---

## 🧠 Usage

### Install Dependencies

```bash
npm install
```

### Run Bot (Main Execution)

```bash
npm run dev
```

---

## ⚙️ Workflow

**Atomic Bundle Sequence**

1. Deploy ERC20 Token
2. Approve Token for NFPM
3. Approve WBNB
4. Create Pool
5. Initialize Pool
6. Add Liquidity
7. Execute Initial Buy
8. Send Bundle → bloXroute

**Four.meme Module**

* Detect new listings or graduated tokens
* Monitor pool creation transactions
* Submit sniping transaction atomically
* Auto-adjust slippage and gas multiplier

**Copy Trade Module**

* Watch target wallets (via WebSocket or BSCScan API)
* Copy buys/sells instantly using your wallet
* Apply configurable multipliers for entry/exit sizes

