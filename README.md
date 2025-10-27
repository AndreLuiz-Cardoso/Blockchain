# 🔗 Blockchain Experiments

Exploratory projects and hands-on experiments in **blockchain** and **decentralized technologies**.  
This repo is for my Web3 work: smart contracts, on-chain games, tokens, vaults, wallet tooling, and a simple blockchain prototype — plus ongoing work on an **algorithmic trading bot** for crypto.

> 🧭 Click the project links below to dive in.

---

## 📚 Topics Included

- **Smart contracts (Solidity basics → advanced)**  
- **Token logic & transactions** (ERC-20, mint/burn, allowances)  
- **On-chain games & CRUD patterns**  
- **Web3 testing (local networks: Anvil/Hardhat)**  
- **Tooling:** Foundry, Hardhat, Remix IDE, MetaMask, Node.js  
- **Security mindset:** reentrancy, access control, events, payments, audit notes  
- **EVM ecosystems & L2s:** zkSync basics, gas & performance  
- **Additional study tracks:** Vyper (basics), DeFi primitives, smart contract auditing approach  
- **Ecosystem:** Member of **BNB Chain Martians**; learning & experimenting on **BNB Chain**

---

## 🚀 Featured Projects

### 1) Solidity Practice Projects – Remix & Foundry  
A collection of Solidity smart contracts built in **Remix** to practice core Web3 concepts; compatible with **Foundry** for local compilation/testing.

**Repo:** <https://github.com/AndreLuiz-Cardoso/Solidity-Remix>

**Contracts (clickable):**
- [`tokenization.sol` – LuxembourgGoldToken (gold-backed ERC-20)](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/tokenization.sol)  
- [`colchao.sol` – ERC-20 Vault (“mattress” vault)](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/colchao.sol)  
- [`StorageFactory.sol` – Factory for `SimpleStorage`](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/StorageFactory.sol)  
- [`SimpleStorage.sol` – Basic storage contract](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/SimpleStorage.sol)  
- [`ParOuImpar.sol` – Even or Odd PvP game](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/ParOuImpar.sol)  
- [`JoKenPo.sol` – Rock/Paper/Scissors with betting & leaderboard](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/JoKenPo.sol)  
- [`BookDatabase.sol` – On-chain book CRUD database](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/BookDatabase.sol)  
- [`AddFiveStorage.sol` – Inheritance/override example](https://github.com/AndreLuiz-Cardoso/Solidity-Remix/blob/main/AddFiveStorage.sol)

**What I practiced here (high-level):**
- ERC-20 design (mint/burn, supply, reserves transparency)
- Vault patterns with ERC-20 approvals
- Factory + inheritance/override
- On-chain games, state machines, payouts, leaderboards
- CRUD with mappings/structs & owner-only modifiers
- Remix deployments; Foundry scripts/tests (optional)

---

### 2) DIOCoin – ERC-20 Token (Educational)
Minimal ERC-20 implementation for learning transfers, approvals, and allowances.

**Repo:** <https://github.com/AndreLuiz-Cardoso/Blockchain/tree/main/Blockchain_Coin>

**Tech & Notes**
- Solidity `^0.8.x`, Remix, MetaMask (Goerli/Sepolia)
- Core interface (`IERC20`), events (`Transfer`, `Approval`)
- Total supply & balances bookkeeping
- Great for understanding *allowance* vs *balance* flows

---

### 3) Bitcoin Wallet Generator (Testnet)
Small Node.js script to generate **Bitcoin testnet** wallets using `bip32`, `bip39`, and `bitcoinjs-lib`.

**Repo:** <https://github.com/AndreLuiz-Cardoso/Blockchain/tree/main/Blockchain_Wallet_Generator>

**What it does**
- Generates a 12-word mnemonic (BIP-39)
- Derives keys (BIP-32) and a testnet P2PKH address
- Prints address, private key (WIF), and seed words
- Perfect for testing integrations with no real funds

---

### 4) Protochain – Minimal Blockchain Prototype
A didactic **blockchain prototype**: hashing, chained blocks, validation, simple server, mining flow, and tests.

**Repo:** <https://github.com/AndreLuiz-Cardoso/Web3-projects/tree/main/protochain>

**What I built / practiced**
- Block hashing & chain linking  
- Validation utilities & unit tests (Jest / Supertest)  
- Simple Node/TypeScript server endpoints  
- Mining flow (proof idea), client mock, error handling  
- Test organization, mocking, and incremental refactors

---

## 🛡️ Security Insights (Summary)

| **Category** | **Best Practices** |
|---|---|
| **Access Control** | Use `Ownable` / `AccessControl` for privileged functions. |
| **Events** | Emit logs for `mint`, `burn`, `deposit`, `withdraw`, and CRUD. |
| **Payments** | Prefer `call{value: ...}` + return check (avoid `transfer` gas limits). |
| **Reentrancy** | Follow *checks-effects-interactions*; use `ReentrancyGuard` where relevant. |
| **Game Fairness** | Use **commit-reveal** to prevent front-running in PvP games. |
| **ERC-20 Safety** | Use `SafeERC20` for token ops; always validate return values. |
| **Transparency** | Asset-backed tokens should include off-chain proofs/audits and clear policies. |

---

## 🧪 Local Dev Tooling

- **Remix IDE**: quick compile/deploy/interaction in the browser  
- **Foundry**: `anvil` (local chain), `forge build/test`, `cast` for interactions  
- **Hardhat**: compilation/testing scripts (when needed)  
- **MetaMask**: testnets (Sepolia, Goerli), local RPCs  
- **Extras**: experimenting with zkSync tooling, gas profiling, and basic Vyper syntax

**Example (Foundry):**
```bash
# run local chain
anvil

# build & test
forge build
forge test -vvv

# example script deploy (if repo/script exists)
forge script script/Deploy.s.sol:Deploy \
  --rpc-url http://127.0.0.1:8545 \
  --private-key <DEV_PRIVATE_KEY> \
  --broadcast -vvvv
```
## 🧠 What I’m Actively Learning / Practicing

- **Solidity proficiency** — clean, readable contracts; inheritance and composition; custom errors; gas-aware design.
- **Standards** — ERC-20 / ERC-721 fundamentals; reserve tracking; RWA tokenization patterns.
- **Testing discipline** — unit tests, fuzzing mindset, edge-case coverage, revert reason assertions.
- **Security mindset** — reentrancy guards, access control, safe payouts, rich eventing/observability.
- **Dev frameworks** — Foundry (deep usage), Hardhat (practical pipelines), Remix (rapid iteration).
- **L2s & performance** — gas/calldata optimization, rollups (zkSync), cross-tooling awareness.
- **Audit approach** — defensive code reading, invariants, “what can break?” analysis, threat modeling.
- **BNB Chain** — ecosystem specifics, tooling, and best practices *(BNB Chain Martians member)*.

---

## 🤖 Algorithmic Trading Bot (Crypto) — In Progress

**Goal:** Build an end-to-end crypto trading assistant (paper/real modes) with modular strategies and exchange connectivity.

**Focus areas**
- **Architecture:** React dashboard, Node/Express backend, WebSocket market feeds.
- **Data & Storage:** MySQL (symbols, wallet, PnL), caching layers, exchange sync.
- **Exchange:** API connectivity, auth flows, rate limits, robust error handling.
- **Strategy:** signal generation (candles/indicators), risk controls, backtesting hooks.
- **Security:** secrets management, permission boundaries, logging/monitoring.

*I’ll publish a dedicated repository as this matures.*

---

## 🗺️ Roadmap (Short List)

- Add **Foundry tests** (fuzz/coverage) across Solidity practice contracts.  
- Improve game fairness with **commit-reveal** & safer payout mechanics.  
- Enrich the **ERC-20 vault** with events, `SafeERC20`, **pausability**, and withdrawal policies.  
- Publish more **BNB Chain** examples and notes.  
- Expand wallet tools (testnet faucets, transaction broadcast, fee estimation).  
- Ship a minimal **DeFi** example (DEX interaction / price feed / oracle demo).

---

## 📂 Quick Links

- 🔸 **Solidity practice set (Remix & Foundry):**  
  <https://github.com/AndreLuiz-Cardoso/Solidity-Remix>

- 🔸 **ERC-20 (educational, minimal):**  
  <https://github.com/AndreLuiz-Cardoso/Blockchain/tree/main/Blockchain_Coin>

- 🔸 **Bitcoin testnet wallet generator:**  
  <https://github.com/AndreLuiz-Cardoso/Blockchain/tree/main/Blockchain_Wallet_Generator>

- 🔸 **Protochain (mini blockchain prototype):**  
  <https://github.com/AndreLuiz-Cardoso/Web3-projects/tree/main/protochain>

---

## 📜 License

Most repositories are under **MIT** unless stated otherwise.  
Each project includes its own **SPDX license identifiers** and README.

---

## 👋 About

**Andre Luiz Cardoso** — Solidity / Web3 developer.  
Building practical projects, learning in public, and exploring EVM ecosystems (incl. **BNB Chain**).  
Open to collaborations and Web3 roles.

**GitHub:** <https://github.com/AndreLuiz-Cardoso>
