# Power Log

Records power-on and power-off history, even in the event of a power failure.

This is useful for *NIX machines without an UPS.

You can monitor if your PC is used when you are away.

## ⭐ Features

⏻ Record power-on and shutdown

🔌 Record power failures

📜 Log in CSV format

## 🤓 Features for nerds

### 🪶 Dependencies ≅ 0

The required packages are already installed in most Linux distributions.

### 🛡️ Protected from process killing!

Simply follow these instructions.

### 🔥 Usable everywhere

You can use in proprietary Linux OS, where you can not install custom packages.

### ⬆️ Updates under your control

You can update the program through your scripts with the `--update` option.

## ⚙️ Installation

### Check if you already have the following packages

* bash
* coreutils
* cron (recommended)
* procps
* wget OR curl (recommended at least one to download updates)

### Download the script

If you have wget:

```bash
wget "https://raw.githubusercontent.com/TonyWhite/PowerLog/main/power-log" -O "power-log"
```

If you have curl:

```bash
curl "https://raw.githubusercontent.com/TonyWhite/PowerLog/main/power-log" -o "power-log"
```

### Install the script with root privileges

```bash
sudo bash power-log --install
```

## 🛠️ Configure

Open cron

```bash
sudo crontab -e
```

Add the rule

```
* * * * * bash -c ' for i in {1..60} ; do power-log --single ; sleep 1s ; done '
```

And this is the better choice with protection from accidentally kill

## 🚀 Usage

Open `/usr/share/power-log/power.log` with Calc of LibreOffice or OpenOffice. The format is CSV (Comma Separated Values).

Enjoy the logs 🪵🦫
