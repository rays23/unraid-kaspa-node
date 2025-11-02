# 🪙 Kaspa Node for Unraid (Rust Implementation)

This repository provides an **Unraid Docker template** for running the official **Kaspa Rust Node** (`kaspanet/rusty-kaspad`) natively on Unraid.  
It was built because **no official Unraid App or template** existed — and most online guides cover only Linux or Windows setups.

This template makes it easy to deploy a fully functional, persistent Kaspa node on Unraid with one click.

---

## 🚀 Features

- Based on **official Rust implementation**: [`kaspanet/rusty-kaspad`](https://github.com/kaspanet/rusty-kaspa)
- Compatible with **Unraid 6.12+**
- **Persistent data** under `/mnt/user/appdata/kaspa`
- **Optimized Docker run parameters** for stable P2P and RPC communication
- **Auto-restart** and clean lifecycle handling on Unraid
- Ready for integration with wallets and mining setups

---

## 🧰 Requirements

| Component | Minimum |
|------------|----------|
| Unraid | 6.12 or newer |
| RAM | 4 GB |
| Storage | 50+ GB free (blockchain data) |
| Network | Ports 16110, 16111, 17110 open |

---

## ⚙️ Quick Start (Manual Deployment)

If you want to run the container manually before adding the Unraid template:

```bash
mkdir -p /mnt/user/appdata/kaspa

docker run -d \
--name kaspa-node \
--restart unless-stopped \
-p 16111:16111 \
-p 16110:16110 \
-p 17110:17110 \
-v /mnt/user/appdata/kaspa:/app/data \
kaspanet/rusty-kaspad:latest \
kaspad \
--utxoindex \
--disable-upnp \
--maxinpeers=64 \
--outpeers=32 \
--yes
