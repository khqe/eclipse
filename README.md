# Guide to Bitz Miner CLI on Eclipse

## What is Bitz?
- The first ePOW commodity token that anyone can mine on Eclipse.
- 5M max supply.
- NOT pre-mined + ZERO team/insider allocations.
- Token address: https://eclipsescan.xyz/token/64mggk2nXg6vHC1qCdsZdEFzd5QGN4id54Vbho4PswCF

# Setup Guide
## Presequities
- Eclipse wallet (.eg `Backpack`) funded with ETH
- Linux Ubuntu Terminal
- Windows users: Must install Linux Ubuntu Terminal using WSL. **[Guide](https://github.com/0xmoei/Install-Linux-on-Windows)**

## Install Dependecies
1. Install Rust
```bash
 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
* When Prompted, Enter `1` and wait unti installation compelete.
```bash
source $HOME/.cargo/env
```
2. Install Solana CLI:
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```
```
solana version
```

## Create CLI wallet
```bash
solana-keygen new
```
* Set a password or skip by pressing `Enter`.
* Save your Seed-Phrase & Public-Key
* Public-Key: Is your node **Eclipse wallet address**.

## Export `Private-key`
```bas
