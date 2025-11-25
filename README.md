
<h1 align="center">ZAIUM Protocol</h1>

**Decentralize power. Shape the future. Sustain the world — block by block.**

---

## 🧩 Overview  
The **ZAIUM Protocol** defines the core rules, data structures, cryptographic primitives and consensus mechanisms that power the ZAIUM blockchain.

This repository documents the technical foundation of the network, including:

- Consensus mechanism (PoW SHA-256)  
- Block structure and validation rules  
- Transaction model (UTXO)  
- Cryptographic algorithms  
- P2P networking and node behavior  
- Governance model and protocol evolution  

This serves as a reference for developers, implementers, auditors and researchers.

---

## 🔐 Cryptographic Foundations  

### **Hashing**  
- SHA-256 (Proof-of-Work hashing engine)  
- Double-SHA-256 for block header hashing  
- Merkle Trees for transaction commitments  

### **Digital Signatures**  
- ECDSA over secp256k1  
- Deterministic signatures (RFC-6979)  
- Secure keypair generation  

### **Address Formats**  
- Base58Check (Legacy)  
- Pay-to-Public-Key-Hash (P2PKH)  
- Pay-to-Script-Hash (P2SH)  
- SegWit (Bech32) planned for native support  

---

## 📦 Block Structure  

Each ZAIUM block contains:

block { version previous_block_hash merkle_root timestamp difficulty_target nonce transactions[] }

### **Block validation rules include:**  
- Must reference a valid previous block  
- Must satisfy the current difficulty target  
- Nonce must meet Proof-of-Work conditions  
- Coinbase transaction must respect issuance rules  
- All transactions must be valid  

---

## ⚙️ Consensus Mechanism  

ZAIUM uses a **Proof-of-Work (PoW) SHA-256** consensus model inspired by Bitcoin, with adjustments for:

- Faster block times (60 seconds)  
- Stability-oriented difficulty retargeting  
- Timestamp protection  
- Double-spend resistance  
- Fork resolution via longest-chain rule  

Future protocol extensions may explore:

- Sidechains  
- Optional privacy enhancements  
- Zero-knowledge based features  
- Layer-2 scaling mechanisms (Lightning compatibility)  

*No PoS or hybrid models are planned.*

---

## 🌐 P2P Network  

Nodes communicate through a decentralized peer-to-peer network using:

- Version handshake  
- Inventory announcements (INV)  
- Block and transaction propagation  
- Node capability negotiation  
- Misbehavior scoring and peer banning  
- Orphan block handling  

The network is designed to be lightweight, resilient and globally scalable.

---

## 📘 Documentation Scope (No fixed schedule)

This repository will progressively document:

### 📌 Core Specifications  
- Consensus rules  
- Block and transaction structure  
- Signature and script validation  
- Difficulty adjustment  

### 📌 Network Protocol  
- Message types  
- Handshakes  
- Inventory propagation  
- Peer discovery  

### 📌 Security & Integrity  
- Threat model  
- Mitigations  
- Replay protection  
- Finality assumptions  

### 📌 Upgrade Path  
- Soft-fork & hard-fork policy  
- Versioning rules  
- Governance structure  

---

## 📜 License  
All protocol documentation will be released under the **MIT License**.

---

## 🌐 Official Links  
- Website: https://zaium.org  
- GitHub Organization: https://github.com/zaium-chain  
- Twitter/X: https://twitter.com/zaiumchain  
- Telegram: https://t.me/zaiumchain  

**ZAIUM — Building the future, block by block.**
