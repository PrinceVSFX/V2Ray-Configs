# Prince VSFX — Быстрый VPN за 1 минуту 🚀

![GitHub last commit](https://img.shields.io/github/last-commit/PrinceVSFX/Vless-Configs)
![GitHub repo size](https://img.shields.io/github/repo-size/PrinceVSFX/Vless-Configs)
![GitHub stars](https://img.shields.io/github/stars/PrinceVSFX/Vless-Configs?style=social)

Готовые VPN-конфигурации с ежедневным обновлением. Подключение занимает меньше минуты.

---

## ⚠️ Дисклеймер

- Автор **НЕ рекламирует** указанные VPN-приложения  
- Все приложения приведены только как примеры  
- Используйте VPN **только в законных целях**

Вы полностью несёте ответственность за использование.

---

## 🚀 Быстрый старт

1. Скопируйте ссылку конфигурации  
2. Импортируйте в VPN-клиент  
3. Запустите тест задержки (ping)  
4. Выберите самый быстрый сервер  
5. Подключитесь  

---

## 🔗 Конфиги

**Основной список (VLESS):**
`link`
**Белый список:**
`link`
---

## ⚙️ Протоколы

`VLESS` · `VMess` · `Trojan` · `Shadowsocks` · `Hysteria` · `Reality`

💡 Если один тормозит — переключитесь на другой

---

## 📱 Рекомендуемые клиенты

- Android: Exclave / v2rayNG  
- iOS: V2Box  
- macOS: Hiddify  
- Windows/Linux: Throne / NekoRay  

---

## 📊 Автообновление (GitHub Actions)

Создайте файл `.github/workflows/update.yml`:

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

💡 Советы
 × Чем ниже ping — тем быстрее VPN
 × Обновляйте конфиги регулярно
 × Пробуйте разные протоколы

⭐ Поставь звезду, если помогло!
