# Voice Decoder Website

Landing page для Voice Decoder.

**Домен:** https://voicedecoder.redorcdron.space
**GitHub Pages:** из папки `/docs`

## Структура

```
docs/
├── index.html          # Главная страница
├── CNAME               # Кастомный домен
├── privacy.html        # Privacy Policy (TODO)
├── terms.html          # Terms of Service (TODO)
├── releases/           # DMG файлы для скачивания
│   └── appcast.xml     # Sparkle update feed
└── assets/
    ├── screenshot.png  # Скриншот приложения (1200×800)
    ├── icon.png        # Иконка для Open Graph
    └── og-image.png    # Превью для соцсетей (1200×630)
```

## Деплой на GitHub Pages

### 1. Push изменений
```bash
git add docs/
git commit -m "Добавить landing page"
git push origin main
```

### 2. Включить GitHub Pages
1. GitHub → Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: `main`, Folder: `/docs`
4. Save

### 3. Настроить DNS в Cloudflare

| Type  | Name         | Content           | Proxy status |
|-------|--------------|-------------------|--------------|
| CNAME | voicedecoder | xecca.github.io   | DNS only     |

### 4. Подтвердить домен в GitHub
1. GitHub → Settings → Pages
2. Custom domain: `voicedecoder.redorcdron.space`
3. Подождать проверку DNS (~5-10 мин)
4. Включить **Enforce HTTPS**

## TODO перед публикацией

- [ ] Скриншот приложения — заменить placeholder
- [ ] Favicon — добавить в `<head>`
- [ ] Open Graph meta tags — для превью в соцсетей
- [ ] Gumroad — создать продукт и обновить ссылку
- [ ] Privacy Policy — создать privacy.html
- [ ] Terms of Service — создать terms.html
