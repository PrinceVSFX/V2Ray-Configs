# Prince VSFX — VPN in 1 Minute 🚀

![GitHub last commit](https://img.shields.io/github/last-commit/PrinceVSFX/Vless-Configs)
![GitHub repo size](https://img.shields.io/github/repo-size/PrinceVSFX/Vless-Configs)
![GitHub stars](https://img.shields.io/github/stars/PrinceVSFX/Vless-Configs?style=social)

Daily updated VPN configs. Connect in under a minute.

---

## ⚠️ Disclaimer

- The author does **NOT promote** any VPN apps listed here  
- Apps are provided only as examples  
- Use VPN **legally only**

You are fully responsible for your actions.

---

## 🚀 Quick Start

1. Copy config link  
2. Import into VPN client  
3. Run ping test  
4. Choose fastest server  
5. Connect  

---

## 🔗 Configs

**Vless (LIST):**
`link`
**White (LIST):**
`link`
---

## ⚙️ Protocols

`VLESS` · `VMess` · `Trojan` · `Shadowsocks` · `Hysteria` · `Reality`

💡 Switch protocol if speed drops

---

## 📱 Recommended Clients

- Android: Exclave / v2rayNG  
- iOS: V2Box  
- macOS: Hiddify  
- Windows/Linux: Throne / NekoRay  

---

## 📊 Auto Update (GitHub Actions)

Create `.github/workflows/update.yml`:

```yaml
name: Update configs

on:
  schedule:
    - cron: '0 * * * *'
  workflow_dispatch:

jobs:
  update:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v3

      - name: Fetch configs
        run: |
          curl -o Vless_list.txt https://raw.githubusercontent.com/PrinceVSFX/Vless-Configs/main/Vless_list.txt

      - name: Commit changes
        run: |
          git config --global user.name "bot"
          git config --global user.email "bot@example.com"
          git add .
          git commit -m "auto update" || echo "no changes"
          git push

name: Update configs
...
git push
```
💡 Tips
 × Lower ping = better speed
 × Update configs regularly
 × Try different protocols

⭐ Star the repo if it helped you!
