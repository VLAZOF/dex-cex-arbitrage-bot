# ⚡ DexCexSpreads: High-Frequency Arbitrage Scanner (Rust)

[![Language](https://img.shields.io/badge/Language-Rust-orange.svg)](https://www.rust-lang.org/)
[![Framework](https://img.shields.io/badge/Async-Tokio-blue.svg)](https://tokio.rs/)
[![Platform](https://img.shields.io/badge/Platform-MEXC%20vs%20DEX-green.svg)]()
[![Telegram](https://img.shields.io/badge/Telegram-Channel-blue.svg)](https://t.me/DexCexSpreads)

## 📖 Overview

**DexCexSpreads** is a high-performance, asynchronous arbitrage scanner written in **Rust**. It monitors price discrepancies between **MEXC Futures** and decentralized exchanges (DEXs) via DexScreener in real-time.

Unlike Python-based bots that suffer from GIL (Global Interpreter Lock) latency, this engine leverages Rust's zero-cost abstractions and the `Tokio` runtime to process 400+ pairs with microsecond-level efficiency.

> **Current Status:** The bot is live and broadcasting signals.
> **Live Demo:** [Join Channel](https://t.me/DexCexSpreads)

---

## 🚀 Key Features

*   **⚡ Ultra-Low Latency:** Written in Rust to minimize the time between price discovery and signal generation.
*   **🧠 Smart Filtering (King Pair Logic):**
    *   Automatically detects the most liquid pair across chains (Ethereum, Solana, BSC, Base).
*   **🛡️ Delisting Protection:**
    *   Real-time synchronization with MEXC API status to ignore delisted or paused assets instantly.
*   **📊 Advanced Metrics:**
    *   Calculates spreads taking into account funding rates and 24h volume.
    *   Monitors liquidity depth to ensure executability of the arbitrage.

---

## 🛠 Tech Stack

*   **Core:** Rust (Edition 2024)
*   **Async Runtime:** Tokio
*   **HTTP Client:** Reqwest (with connection pooling)
*   **Data Handling:** Serde / Serde JSON
*   **Architecture:**
    *   Multi-threaded monitoring cycles.
    *   Non-blocking signal dispatching (Fire-and-Forget logging).
    *   Atomic state management (`RwLock`).

---

## ⚠️ Source Code Availability

This repository serves as the documentation and issue tracker for the project.

Due to the nature of arbitrage strategies, **the source code is currently private** to prevent strategy saturation and maintain edge for our community members.

However, the bot is **free to use** for the public. We believe in democratizing access to market inefficiencies.

### How to use:
1.  Go to the Telegram channel: **[t.me/DexCexSpreads](https://t.me/DexCexSpreads)**
2.  Subscribe.
3.  Receive real-time notifications when a spread > 5% is detected.

---

## 🤝 Contact & Support

If you found a bug or have a feature request, please open an Issue in this repository.

For discussion and live signals, join our community:
👉 **[t.me/DexCexSpreads](https://t.me/DexCexSpreads)**
