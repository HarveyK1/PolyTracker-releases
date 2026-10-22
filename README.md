# PolyTracker

[![Stars](https://img.shields.io/github/stars/HarveyK1/Rise-Alarm?style=for-the-badge)](https://github.com/HarveyK1/Rise-Alarm/stargazers)
[![Watchers](https://img.shields.io/github/watchers/HarveyK1/Rise-Alarm?style=for-the-badge)](https://github.com/HarveyK1/Rise-Alarm/watchers)
[![Forks](https://img.shields.io/github/forks/HarveyK1/Rise-Alarm?style=for-the-badge)](https://github.com/HarveyK1/Rise-Alarm/forks)
[![Total Views](https://hits.sh/github.com/HarveyK1/Rise-Alarm.svg?view=total&style=for-the-badge&label=total%20views)](https://hits.sh/github.com/HarveyK1/Rise-Alarm/)

A desktop tracker for [Polymarket](https://polymarket.com) prediction markets, for Windows.
It shows live prices and order books, your portfolio and P&L, top traders and whales, news matched
to markets, and alerts on your desktop or phone.

**It only reads public data.** It never asks for a private key, seed phrase or password, and it
can't place, cancel or sign trades.

### [⬇ Download the latest version](https://github.com/HarveyK1/PolyTracker-releases/releases/latest)

Under **Assets**, download `PolyTracker-<version>-windows-x64.zip`.

This repository holds the released versions only.

---

## Install

1. **Extract the zip:** right-click it, then **Extract All**. The installer doesn't work from
   inside the zip.
2. In the extracted folder, double-click **Install PolyTracker**.
3. Windows may warn you, because PolyTracker isn't signed with a paid certificate:
   - *Open File – Security Warning*: click **Run**.
   - *Windows protected your PC*: click **More info**, then **Run anyway**.
4. PolyTracker opens when it's done. It's in your Start menu and on your desktop.

It installs just for you, in `%LOCALAPPDATA%\Programs\PolyTracker`, and needs no administrator
rights. You can delete the zip and the extracted folder afterwards.

**Needs:** Windows 10 or 11 (64-bit), and Microsoft's
[Visual C++ Redistributable (x64)](https://aka.ms/vs/17/release/vc_redist.x64.exe), which most PCs
already have. The installer checks for it and tells you if it's missing.

## Updates

PolyTracker looks for a new version when it starts and every few hours. When one is out,
**Update to …** appears at the bottom right of the window. Click it to see what's new, then
**Update now**. PolyTracker downloads the new version, checks it, closes, installs it and reopens.
Your data and settings are kept.

You can also check yourself in **Settings → About → Check now**.

## Uninstall

**Settings → Apps → Installed apps → PolyTracker → Uninstall**. It asks whether to delete your
data too (watchlists, followed wallets, alert rules, settings, and saved sign-ins). If you keep it,
it's there if you install PolyTracker again.

## Privacy and safety

- **Read-only:** it reads Polymarket's public data and public wallet activity. Wallet addresses and
  positions on Polymarket are public; tracking one only reads what anyone can see on polymarket.com.
- **Your data stays on your PC,** in `%LOCALAPPDATA%\PolyTracker`. There's no account and no usage
  tracking.
- **What it connects to:**
  - Polymarket, for markets and wallets
  - the news sources you turn on
  - a public Polygon node, for a wallet's cash balance
  - GitHub (this page), to look for updates
  - X, Discord and Telegram, only if you connect them yourself (those sign-ins and keys are kept in
    Windows Credential Manager)
- **Not financial advice:** estimates, "edges" and suggested sizes are calculations from public
  prices, not recommendations.

## Checking a download

Each release lists the zip's SHA-256 checksum, and has a `.sha256` file beside it. PolyTracker's
updater checks this itself. To check a zip you downloaded by hand, run this in PowerShell and
compare the result:

```powershell
Get-FileHash .\PolyTracker-<version>-windows-x64.zip -Algorithm SHA256
```

## Help

PolyTracker has a full guide built in: open **Wiki** at the bottom left. If something goes wrong,
**Logs → Export logs** saves a log file you can send along with a description of the problem.
