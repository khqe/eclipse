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
**1. Install Packages**
```bash
sudo apt-get update && sudo apt-get upgrade -y

sudo apt install screen curl nano  -y
```
**2. Install Rust**
```bash
 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
* When Prompted, Enter `1` and wait unti installation compelete.
```bash
source $HOME/.cargo/env
```
**3. Install Solana CLI:**
```bash
curl --proto '=https' --tlsv1.2 -sSfL https://solana-install.solana.workers.dev | bash
```
* Close and reopen your Terminal.
```
solana version
```
**4. Switch RPC**
```bash
solana config set --url https://mainnetbeta-rpc.eclipse.xyz/
```

## Wallet CLI
### 1. Create a CLI wallet
```bash
solana-keygen new
```
* Set a password or skip by pressing `Enter`.
* Save your Seed-Phrase & Public-Key
* `Public-Key`: Is your node **Eclipse wallet address**.

### 2. Export `Private-key`

1- Find Keypair path:
```bash
solana config get
```
* It gives your Keypair path like this: `~/.config/solana/id.json`

2- Export `Private-key`:
```bash
cat ~/.config/solana/id.json
```
* The exported array is your `Private-Key`, Save it.

### 3. Import and Fund Node Wallet
* Import `Private-Key` into your `Backpack` wallet.
* Fund it with `ETH` on `Eclipse` Network

## Install Bitz
```bash
cargo install bitz
```

## ## Install Bitz
