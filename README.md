# 🎁 GifteWin RANDOM

Профессиональный Telegram-бот + Mini App для розыгрышей подарков, NFT и Stars.

## Что умеет

- Создание розыгрышей (Gift / Stars / NFT)
- Прикрепление **фото или GIF** приза
- Живой таймер итогов
- Ники участников + % шанса в реальном времени
- Взвешенный рандом (баллы удачи от рефералов)
- Автовыбор победителей
- Экран победителей с призом
- Кнопка канала `t.me/GifteWin`
- Boost канала (опционально)
- Тёмный премиум-дизайн (стили встроены — не ломается)

## Быстрый старт бота

```bash
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env
# Заполни BOT_TOKEN, ADMIN_IDS, BOT_USERNAME
python -m bot.main
```

## Mini App

Файл `webapp/index.html` — **самодостаточный** (CSS и JS внутри).

### Как подключить к боту / каналу

1. Залей `webapp/index.html` на хостинг:
   - GitHub Pages
   - Cloudflare Pages
   - Vercel
   - любой статический хост

2. В **@BotFather**:
   - `/mybots` → твой бот → **Bot Settings** → **Menu Button**
   - Укажи URL Mini App
   - Или создай кнопку Web App в клавиатуре бота

3. Добавь бота **админом в канал** `@GifteWin` (или свой), чтобы:
   - публиковать розыгрыши
   - проверять подписку / Boost (Bot API 7+)

4. В `.env` укажи:
```
CHANNEL_USERNAME=GifteWin
CHANNEL_LINK=https://t.me/GifteWin
BOT_USERNAME=твой_бот
```

## Как победитель видит приз

- После окончания таймера бот/приложение автоматически выбирает победителей
- Победитель получает уведомление с названием приза
- В карточке розыгрыша показывается блок **«🎉 Победители»** + описание приза + медиа (если было)
- Создатель передаёт подарок/NFT/Stars вручную (бот честно проводит розыгрыш)

## Рефералы

Ссылка: `https://t.me/ТВОЙ_БОТ?start=ref_USER_ID`  
За друга: +10 баллов удачи → выше шанс.

## Структура

```
GifteWin-RANDOM/
├── bot/           # aiogram 3 бот
├── webapp/
│   └── index.html # Mini App (всё в одном файле)
├── requirements.txt
├── .env.example
└── README.md
```

MIT
