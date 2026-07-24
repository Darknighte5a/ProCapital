# Changelog

All notable changes to **ProCapital** will be documented in this file.

فرمت این فایل بر اساس [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) است.

---
## [9.42] - 2026-07-24

Bug Fixes


## [9.41] - 2026-01-15

### ✨ Added / اضافه شد
- سیستم Partial Exit برای سفارشات Limit/Stop (فعال‌سازی خودکار پس از پر شدن سفارش)
- Partial Exit system for Limit/Stop orders (auto-activates once order is filled)
- پشتیبانی از تشخیص فیل شدن سفارش با `OnTradeTransaction`
- Order fill detection via `OnTradeTransaction`

### 🔧 Changed / تغییر کرد
- بهینه‌سازی به‌روزرسانی پنل پوزیشن‌ها (Smart Update بجای رفرش کامل)
- Optimized position panel updates (smart update instead of full refresh)

### 🐛 Fixed / رفع شد
- رفع مشکل جابجایی نادرست پنل‌ها هنگام تغییر اندازه چارت
- Fixed incorrect panel positioning on chart resize

---

## [9.0] - 2025-12-01

### ✨ Added
- دکمه Risk-Free برای انتقال خودکار SL به نقطه ورود
- Risk-Free button for automatic SL-to-entry adjustment
- تایمر شمارش معکوس کندل
- Candle countdown timer
- سیستم ریست کامل با کلیدهای Ctrl و R
- Full reset system via Ctrl and R hotkeys

---

## [8.0] - 2025-10-15

### ✨ Added
- نسخه اولیه پنل معاملاتی
- Initial trading panel release
- محاسبه خودکار حجم بر اساس ریسک
- Automatic lot calculation based on risk
- محدودیت سود/زیان روزانه
- Daily profit/loss limits
