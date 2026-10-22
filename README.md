# App Catalog

Публичный каталог приложений портфеля — источник данных для кросс-промо во всех приложениях.

## URL для приложений

```
https://raw.githubusercontent.com/unlying-debia/app-catalog/main/catalog.json
```

## Формат

Каждая запись: `id`, `title`, `desc`, `emoji`, `icon` (URL или null), `status` (`planned`/`published` — промо показывает только `published`), `stores` (ссылки Google Play / RuStore / App Store / Telegram-бот).

## Правила обновления

1. Когда приложение публикуется в сторах — заполнить его `stores`-ссылки, поставить `status: "published"`, положить иконку 256×256 в `icons/<id>.png` и прописать её URL в `icon`.
2. Коммит в `main` сразу доступен всем приложениям (raw-CDN, кэш ~5 минут; приложения кэшируют каталог на 24 ч).

Подробности интеграции — гайд `CROSS-PROMO.md` в приватном репозитории `app-factory`.
