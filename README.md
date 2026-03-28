# ![SmartieCoin](http://lucky-pool.co.uk/img/coin/icon/smt.png) SmartieCoin (SMT) Wallet Generator

A fully client-side, offline-capable wallet generator for **Smartiecoin (SMT)** — a secondary coin in the Ethernova ecosystem focused on CPU mining, privacy (CoinJoin/Tor), and deterministic masternodes.

🔗 **Live Demo:** [https://syabiz.github.io/pages/SmartieCoin-Wallet-Generator/](https://syabiz.github.io/pages/SmartieCoin-Wallet-Generator/)

---

## ✨ Features

| Feature | Description |
|---|---|
| ✨ **Generate New Wallet** | Create a fresh SMT wallet with a BIP39 12-word mnemonic seed phrase, public address, private key (WIF & hex), and public key |
| 🔤 **Restore from Mnemonic** | Recover an existing wallet from a 12-word BIP39 seed phrase with optional BIP39 passphrase and derivation index |
| 🔑 **Restore from Private Key** | Derive a public address from a WIF or hex-encoded private key |
| 🖨 **Paper Wallet Generator** | Generate a printable paper wallet with QR codes for both public address and private key |
| 🎯 **Vanity Address Generator** | Search for a custom SMT address that starts with, ends with, or contains a specific pattern. Supports case-sensitive mode |

---

## 🖥️ Screenshots

> Live preview available at the demo link above.

---

## 🚀 Getting Started

### Online (No Installation)

Simply open the live demo link in any modern browser. Everything runs in your browser — no data is ever sent to a server.

### Offline Usage

This tool is designed to work fully offline. To use it without an internet connection:

1. **Download `index.html`** from this repository.
2. **Download the required external libraries manually** (see [Dependencies](#-dependencies) below).
3. **Download the required Google Fonts** or replace them with local alternatives.
4. Place all files in the same directory and update the `<script src="">` and `<link href="">` paths in the `<head>` section of `index.html` to point to the local files.
5. Open `index.html` in your browser.

---

## 📦 Dependencies

All dependencies are loaded from CDN by default. For offline use, download them manually:

| Library | Version | CDN URL | Purpose |
|---|---|---|---|
| **CryptoJS** | 4.2.0 | [cdnjs](https://cdnjs.cloudflare.com/ajax/libs/crypto-js/4.2.0/crypto-js.min.js) | SHA256 hashing, HMAC, AES |
| **QRCode.js** | 1.0.0 | [cdnjs](https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js) | QR code generation for addresses |

### Fonts (Google Fonts)

| Font | Weights | Purpose |
|---|---|---|
| **Outfit** | 400, 600, 700, 800 | Headings, labels, monospace values |
| **Manrope** | 400, 500, 600, 700, 800 | Body text, UI elements |

For offline use, download fonts from [Google Fonts](https://fonts.google.com/) or use a font downloader tool and update the `<link>` tags in `<head>` accordingly.

---

## 🔐 Security & Privacy

- **100% client-side** — all cryptographic operations happen in your browser using the Web Crypto API.
- **No network requests** are made during wallet generation. All entropy comes from `crypto.getRandomValues()`.
- **No data is stored** — nothing is saved to localStorage, cookies, or any server.
- **Recommended:** For maximum security, use this tool on an **air-gapped (offline) machine**, especially when generating wallets that will hold significant funds.
- **Never share your private key or seed phrase** with anyone.

---

## 🧪 Cryptographic Standards

- **BIP39** — Mnemonic seed phrase generation (12 words, 128-bit entropy + checksum)
- **BIP32/BIP44** — Hierarchical Deterministic (HD) wallet derivation
- **Base58Check** — SMT address encoding
- **WIF** — Wallet Import Format for private keys
- **SECP256k1** — Elliptic curve for key pair generation

---

## 🗂️ File Structure

```
SmartieCoin-Wallet-Generator/
└── index.html      # Single self-contained HTML file (all CSS and JS included)
```

This project is intentionally a **single-file application** — all styles and scripts are inlined for maximum portability and ease of offline use.

---

## 🌐 About Smartiecoin (SMT)

Smartiecoin (SMT) is a secondary cryptocurrency in the **Ethernova ecosystem**, designed with a focus on:

- ⛏️ **CPU Mining** — Fair and decentralized mining accessible to everyday hardware
- 🔒 **Privacy** — Integration with CoinJoin and Tor for enhanced transaction privacy
- 🖥️ **Masternodes** — Deterministic masternode support for network stability and governance

For more information, visit [smartiecoin.com](https://smartiecoin.com).

---

## ☕ Support

If this tool has been helpful to you, perhaps there's a reward of a cup of coffee and a pack of cigarettes for me? 😄

| Network | Address |
|---|---|
| <img src="https://smartiecoin.com/assets/logo-horizontal.png" width="20"/> Smartie (SMT) | `SSdwnEwNVNm2f3zrfC383sBwwq7CJ7Lkvj` |
| ⟠ Ethernova (NOVA) | '0x512936ca43829C8f71017aE47460820Fe703CAea' |
| ₿ Bitcoin (BTC) | `bc1qn6t8hy8memjfzp4y3sh6fvadjdtqj64vfvlx58` |
| ⟠ Ethereum (ETH) | `0x512936ca43829C8f71017aE47460820Fe703CAea` |
| ◎ Solana (SOL) | `6ZZrRmeGWMZSmBnQFWXG2UJauqbEgZnwb4Ly9vLYr7mi` |

Every bit of support is deeply appreciated! 🙏

---

## 📄 License

This project is open source. See [LICENSE](LICENSE.md) for details.
