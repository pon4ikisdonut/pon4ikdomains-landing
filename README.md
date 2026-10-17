# pon4ikdomains landing page (sub.pon4ikisdonut.pp.ua)

Минималистичный лендинг сервиса **pon4ik subdomains**, оптимизированный для хостинга на **GitHub Pages** с кастомным доменом `sub.pon4ikisdonut.pp.ua`.

## 📁 Структура
* `index.html` — легковесная минималистичная страница с интерактивным калькулятором стоимости в Telegram Stars, каталогом зон и фичами.
* `CNAME` — содержит `sub.pon4ikisdonut.pp.ua` для автоматической привязки в GitHub Pages.
* `.nojekyll` — отключает обработку Jekyll для максимальной скорости отдачи статики.

## 🚀 Как задеплоить на GitHub Pages:
1. Создайте репозиторий на GitHub (например, `pon4ikdomains-landing`).
2. Запушьте файлы из этой папки:
   ```bash
   git init
   git add .
   git commit -m "Initial commit for pon4ikdomains landing"
   git branch -M main
   git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/<REPO_NAME>.git
   git push -u origin main
   ```
3. В настройках репозитория:
   * **Settings** ➔ **Pages**.
   * **Branch**: `main`, папка `/ (root)`.
   * **Custom domain**: проверьте, что указан `sub.pon4ikisdonut.pp.ua`.
4. В Cloudflare для зоны `pon4ikisdonut.pp.ua`:
   * Создайте запись:
     * **Type**: `CNAME`
     * **Name**: `sub`
     * **Target**: `<YOUR_GITHUB_USERNAME>.github.io`
     * **Proxy**: `DNS only` (⚪) во время верификации GitHub, затем можно включить `Proxied` (🟠).
