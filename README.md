# Pre-compiled CCMiner for Termux:
This is a WIP repo for pre-compiled ccminer binaries with latest termux(v0.118.0) and latest clang(v17.0.6).

# **`Disclaimer: I accept no warranties or liabilities on this repo. Do it at your own risk!!!`**

# **`This is for ARM Cortex-A73 & Cortex-A53`**

# Installation:
1. Download & install latest arm64-v8a [Termux](https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk):
```
https://github.com/termux/termux-app/releases/download/v0.118.0/termux-app_v0.118.0+github-debug_arm64-v8a.apk
```
2. Get Termux ready:
- Type `y` then enter key in any prompts!
```
pkg update -y && pkg upgrade -y
pkg install libjansson wget nano -y
```
3. Download ccminer, config, start:
```
mkdir ccminer && cd ccminer
wget https://github.com/TvrdyChlast/ccminer/raw/main/ccminer
wget https://github.com/TvrdyChlast/ccminer/raw/main/config.json
wget https://github.com/TvrdyChlast/ccminer/raw/main/start.sh
chmod +x ccminer start.sh
```
# Usage:

1. Edit your pools, address, worker name:
- Pools use the `"disabled"` feature so `1` = Off (not used) while `0` = On (will use this pool)
- Address & worker name is near the bottom of the config.json in format `address here.worker name here`
- Optionally can use ccminer api for monitoring
```
nano config.json
```
2. Start ccminer with:
```
~/ccminer/start.sh
```
3. autorun:
```
nano /data/data/com.termux/files/usr/etc/bash.bashrc

```
Add

```
bash /data/data/com.termux/files/home/ccminer/start.sh
```
