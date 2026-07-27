# LE DESIGNER SHOP — Telegram Mini App

A single-file Telegram Mini App shop for a French design/web services business.

## Stack
- Pure HTML/CSS/JS — no build step
- Firebase (Firestore + Auth) for product overrides, orders, and admin login
- Telegram WebApp SDK for user identity and haptics
- GSAP for animations

## How to run
```
python3 -m http.server 5000
```
Workflow: **Start application** (auto-configured).

## Key details
- **Single file**: all code lives in `index.html`
- **Firebase project**: `ledesigner-3bca3` — config is hardcoded in the JS
- **Admin panel**: tap the logo 5× fast to open; requires Firebase email/password login
- **Products**: defined in the `PRODUCTS` array in JS; admins can override images/prices/descriptions via Firestore (`shop/products`)
- **Telegram identity**: `tg.initDataUnsafe.user` provides name, username, ID, and photo — displayed on the profile page. Falls back gracefully in a browser preview.

## User preferences
- Background: neon/fluorescent green theme (`--bg: #020d04`, `--neon: #39ff6e`)
- Profile page shows each Telegram user's real photo, full name, username, and ID
