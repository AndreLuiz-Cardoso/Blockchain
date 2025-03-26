# 💼 Bitcoin Wallet Generator (Testnet)

A lightweight and educational tool to **generate Bitcoin testnet wallets** using JavaScript and widely adopted libraries like `bip32`, `bip39`, and `bitcoinjs-lib`.

> 🔐 Perfect for testing, development, and learning how real Bitcoin wallets work — with **no risk and no real funds** required.

---

## ❓ What is This?

This project simulates the generation of a Bitcoin wallet on the **testnet** (Bitcoin's public testing blockchain).  
It demonstrates how to generate:

- A **12-word mnemonic phrase** (BIP39)
- A **private key** and **public key** (BIP32)
- A **SegWit-compatible address** (P2PKH format, using derivation path `m/49'/1'/0'/0`)

All outputs are printed in the console, ready for use in testing environments or dApp development.

---

## ✨ Features

- 🔐 **Testnet-Compatible Wallets**  
  Derives wallets using path `m/49'/1'/0'/0` (SegWit-compatible)

- 🧠 **Mnemonic Phrase (BIP39)**  
  Secure 12-word recovery phrase generation

- 🔑 **Private & Public Key Derivation (BIP32)**  
  Hierarchical key structure from seed phrase

- 🏦 **Bitcoin Address (P2PKH format)**  
  Standard address for receiving testnet funds

- 🖥️ **Console Output**  
  Easy-to-read display of all generated data

---

## 🛠️ Tech Stack

- **Node.js** – Runtime environment  
- **bip32** – HD wallet derivation  
- **bip39** – Mnemonic creation and seed handling  
- **bitcoinjs-lib** – Key/address generation and Bitcoin logic

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/bitcoin-wallet-generator.git
cd bitcoin-wallet-generator
``` 

---
### 2. Install dependencies

```bash
npm install bip32 bip39 bitcoinjs-lib
```

---

### 3. Run the script
```bash
node createwallet.js
```

---
## 📋 Output Example

```
Wallet generated
Address:      2N9XkY...   (SegWit-compatible testnet address)
Private Key:  cU9sTz...   (WIF format)
Seed:         turtle lava drop talent ... voice
```
---

## 🧪 Use Cases

- 🔬 Test Bitcoin applications with real logic and no cost  
- 🧱 Develop dApps, wallets, or blockchain integrations  
- 🎓 Learn how HD wallets, keys, and addresses are created  
- 🔁 Practice signing or broadcasting transactions using testnet coins

🔗 [Get free testnet BTC here (faucet)](https://testnet-faucet.mempool.co/)

---

## 📄 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).  
Feel free to use, modify, and distribute.

---

## 🤝 Contributions

Contributions are welcome!  
Feel free to fork this repo, suggest improvements, or open an issue for ideas and questions.

---

## 📚 Learn More

- [BIP39 Specification – Mnemonic Phrase](https://github.com/bitcoin/bips/blob/master/bip-0039.mediawiki)  
- [BIP32 – Hierarchical Deterministic Wallets](https://github.com/bitcoin/bips/blob/master/bip-0032.mediawiki)  
- [bitcoinjs-lib Documentation](https://github.com/bitcoinjs/bitcoinjs-lib)

---
