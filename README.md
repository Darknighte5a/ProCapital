# ProCapital
A modern MetaTrader 5 Expert Advisor focused on professional risk management, position management and fast trade execution through an interactive trading panel.
<div align="center">

# ⚡ ProCapital

### Advanced MT5 Trading Panel & Risk Management EA

[![Platform](https://img.shields.io/badge/platform-MetaTrader%205-orange.svg)](https://www.metatrader5.com/)
[![License](https://img.shields.io/badge/license-Proprietary-red.svg)](LICENSE)
[![Language](https://img.shields.io/badge/language-MQL5-green.svg)](https://www.mql5.com/)

**[فارسی](#فارسی) | [English](#english)**

</div>

---

<a name="فارسی"></a>
## 🇮🇷 فارسی

### 📖 معرفی

**ProCapital** یک اکسپرت پیشرفته برای متاتریدر ۵ است که یک پنل معاملاتی کامل، حرفه‌ای و بصری روی چارت شما ارائه می‌دهد. این ابزار برای معامله‌گرانی طراحی شده که به دنبال مدیریت ریسک دقیق، اجرای سریع معاملات و کنترل کامل روی پوزیشن‌های باز خود هستند.

### ✨ ویژگی‌های اصلی

#### 🎯 پنل معاملاتی هوشمند
- محاسبه خودکار حجم معامله (لات) بر اساس درصد ریسک تعیین‌شده
- پشتیبانی کامل از سفارشات **Market**، **Limit** و **Stop**
- امکان جابجایی (Drag & Drop) پنل به هر نقطه از چارت
- نمایش لحظه‌ای اسپرد و مبلغ ریسک

#### 📊 مدیریت پوزیشن (Position Manager)
- نمایش تمام پوزیشن‌های باز با سود/زیان لحظه‌ای (مبلغ و درصد)
- دکمه بستن سریع هر پوزیشن با یک کلیک
- دکمه **Risk-Free** برای انتقال خودکار حد ضرر به نقطه ورود + بافر امن
- نمایش مجموع سود/زیان کل پوزیشن‌های باز

#### 📈 خطوط تعاملی روی چارت
- خطوط قابل‌درگ برای **Take Profit**، **Stop Loss**، **Entry** و **Partial Exit**
- نمایش لحظه‌ای مبلغ سود/زیان هر خط بر حسب دلار
- محاسبه خودکار نسبت **Risk:Reward**

#### 🎯 خروج پله‌ای (Partial Exit)
- تعریف یک قیمت هدف برای بستن بخشی از حجم معامله
- کار می‌کند حتی روی سفارشات Limit/Stop (پس از پر شدن سفارش، قانون به‌صورت خودکار فعال می‌شود)
- ردیابی مستقل از باز یا بسته بودن پنل

#### 🛡️ مدیریت ریسک حرفه‌ای
- محدودیت حداکثر ضرر روزانه (خودکار بستن همه پوزیشن‌ها)
- محدودیت حداکثر سود روزانه (قفل سود)
- بستن خودکار پوزیشن‌ها قبل از تعطیلات آخر هفته
- فیلتر ساعت معاملاتی (فقط در بازه‌های مشخص معامله انجام شود)

#### ⏱️ سایر امکانات
- تایمر شمارش معکوس تا بسته شدن کندل فعلی
- طراحی رنگی قابل شخصی‌سازی کامل
- پشتیبانی از چند چارت هم‌زمان با قابلیت ریست گروهی (کلید `R`)
- بهینه‌سازی شده برای مصرف کم منابع

### 🖼️ تصاویر

> screenshots
>
> 
### ⚙️ نصب و راه‌اندازی

1. فایل `ProCapital.mq5` را دانلود کنید.
2. آن را در مسیر زیر کپی کنید:
3. متاتریدر ۵ را باز کرده و از منوی **Navigator**، روی فایل EA راست‌کلیک کرده و **Compile** بزنید (یا در MetaEditor با کلید `F7`).
4. اکسپرت را از Navigator روی چارت مورد نظر بکشید.
5. در تنظیمات EA، گزینه **Allow Algo Trading** را فعال کنید.
6. از دکمه‌های شناور **Trade** و **Pos** در گوشه چارت برای باز کردن پنل‌ها استفاده کنید.

### 📋 تنظیمات ورودی (Inputs)

| گروه | پارامتر | توضیح | مقدار پیش‌فرض |
|---|---|---|---|
| **RISK** | `iRisk` | درصد ریسک هر معامله نسبت به بالانس | 0.5 |
| | `iMaxDayLoss` | حداکثر درصد ضرر مجاز روزانه | 5.0 |
| | `iMaxDayProfit` | حداکثر درصد سود روزانه (قفل سود) | 15.0 |
| **FILTERS** | `iTimeFilter` | فعال‌سازی فیلتر ساعت معاملاتی | true |
| | `iStartHour` / `iEndHour` | بازه ساعتی مجاز معامله | 8 - 20 |
| | `iCloseWknd` | بستن خودکار قبل از آخر هفته | true |
| | `iMagic` | شماره مجیک اختصاصی EA | 20240101 |
| **TIMER** | `iShowTimer` | نمایش تایمر کندل | true |
| **COLORS** | `iClrBuy` / `iClrSell` | رنگ دکمه‌های خرید/فروش | سبز / قرمز |
| | `iClrTP` / `iClrSL` | رنگ خطوط TP و SL | سبز / قرمز |

### 🕹️ راهنمای استفاده

- **باز کردن پنل معاملاتی:** دکمه شناور `Trade` گوشه چارت
- **باز کردن پنل پوزیشن‌ها:** دکمه شناور `Pos` گوشه چارت
- **ریست کامل پنل (چارت فعلی):** کلید `Ctrl`
- **ریست همه چارت‌های باز:** کلید `R`
- **جابجایی پنل‌ها:** روی نوار عنوان (هدر) پنل کلیک نگه‌دارید و بکشید
- **تنظیم خطوط قیمتی:** روی خط کلیک کرده و به بالا/پایین بکشید

### ⚠️ سلب مسئولیت

این ابزار صرفاً جهت کمک به مدیریت و اجرای سریع‌تر معاملات طراحی شده و **هیچ تضمینی برای سودآوری ندارد**. معامله در بازارهای مالی دارای ریسک از دست دادن سرمایه است. استفاده از این ابزار بر عهده و مسئولیت کامل کاربر است. سازنده هیچ مسئولیتی در قبال ضرر و زیان‌های احتمالی نمی‌پذیرد.

### 📜 مجوز استفاده

این پروژه تحت مجوز اختصاصی منتشر شده است. برای جزئیات به فایل [LICENSE](LICENSE) مراجعه کنید.

### 📞 ارتباط با ما

- **Telegram:** [@Darknighte5a](https://t.me/Darknighte5a)
### حمایت از من
آدرس ولت بیت کوین : bc1ql6fwvu4dwsv32fs9tkh454y8hrd0gs6esaade24t9hexwnnq6lkskarqkf
آدرس لایتینگ : lnbc1p49jdtdpp52d82np6sy49mqgpmy3dmuhk5cfxjlm9sywsfrlralg57fqv42c6qdqqcqzzgxqyz5vqrzjqf0wu22xsefd8gzu0m9n93g2khea86l6yy26en9v46g9e6hk7v9z8m287z05kagmsuqqqqryqqqqthqqpyrzjqfwdd2w9y5ra5z3m4qetfa5ccu6432xfuvk6zrvg9vxwltvukd48dm287z05kagmsuqqqqryqqqqthqqpysp5sxtsp3gmh8rnk3c7hsynqsuq20tnhhv470200tjnk8rnc3q6akls9qrsgqegmhm5w9f2dkdyr6jkltzujqnq3xh2gclt3psmxuk5h7x47mpe63fm9q4533xm6822fm3h59567gmyjah0vynzygpkmsksnhqg0wn2gp383jfc
آدرس شبکه اتریوم و بی ان بی : 0x2C2f11eF7203D66fEb4c4f594F9f3a2A40394f3e
آدرس شبکه ترون : TDzq7z4ZkQTsAAzRxy1JXKJ985HRhAMKsD
---

<a name="english"></a>
## 🇬🇧 English

### 📖 Overview

**ProCapital** is an advanced MetaTrader 5 Expert Advisor that provides a complete, professional, and visual trading panel directly on your chart. It's designed for traders who need precise risk management, fast trade execution, and full control over their open positions.

### ✨ Key Features

#### 🎯 Smart Trading Panel
- Automatic lot size calculation based on defined risk percentage
- Full support for **Market**, **Limit**, and **Stop** orders
- Drag & drop the panel anywhere on the chart
- Real-time spread and risk amount display

#### 📊 Position Manager
- View all open positions with live P&L (amount and percentage)
- One-click close button for each position
- **Risk-Free** button to automatically move stop-loss to entry + safety buffer
- Total floating P&L summary of all open positions

#### 📈 Interactive Chart Lines
- Draggable lines for **Take Profit**, **Stop Loss**, **Entry**, and **Partial Exit**
- Real-time dollar P&L display on each line
- Automatic **Risk:Reward** ratio calculation

#### 🎯 Partial Exit System
- Define a target price to close part of your position's volume
- Works even with Limit/Stop orders (rule activates automatically once the order is filled)
- Independent tracking, regardless of panel visibility

#### 🛡️ Professional Risk Management
- Maximum daily loss limit (auto-closes all positions)
- Maximum daily profit limit (profit lock)
- Automatic position closure before weekend
- Trading hours filter (trade only within a defined time window)

#### ⏱️ Additional Features
- Candle countdown timer
- Fully customizable color scheme
- Multi-chart support with global reset (press `R`)
- Optimized for low resource usage

### 🖼️ Screenshots

### ⚙️ Installation

1. Download the `ProCapital.mq5` file.
2. Copy it to:
3. Open MetaTrader 5, right-click the EA in the **Navigator** panel and select **Compile** (or press `F7` in MetaEditor).
4. Drag the EA from the Navigator onto your desired chart.
5. In the EA settings, enable **Allow Algo Trading**.
6. Use the floating **Trade** and **Pos** buttons at the corner of the chart to open the panels.

### 📋 Input Parameters

| Group | Parameter | Description | Default |
|---|---|---|---|
| **RISK** | `iRisk` | Risk percentage per trade relative to balance | 0.5 |
| | `iMaxDayLoss` | Maximum allowed daily loss percentage | 5.0 |
| | `iMaxDayProfit` | Maximum daily profit percentage (profit lock) | 15.0 |
| **FILTERS** | `iTimeFilter` | Enable trading hours filter | true |
| | `iStartHour` / `iEndHour` | Allowed trading hour range | 8 - 20 |
| | `iCloseWknd` | Auto-close positions before weekend | true |
| | `iMagic` | EA's unique magic number | 20240101 |
| **TIMER** | `iShowTimer` | Show candle countdown timer | true |
| **COLORS** | `iClrBuy` / `iClrSell` | Buy/Sell button colors | Green / Red |
| | `iClrTP` / `iClrSL` | TP and SL line colors | Green / Red |

### 🕹️ Usage Guide

- **Open Trade Panel:** Click the floating `Trade` button at the chart corner
- **Open Position Panel:** Click the floating `Pos` button at the chart corner
- **Full reset (current chart):** Press `Ctrl`
- **Reset all open charts:** Press `R`
- **Move panels:** Click and hold the panel header, then drag
- **Adjust price lines:** Click on a line and drag it up/down

### ⚠️ Disclaimer

This tool is designed solely to assist with trade management and faster execution and **comes with no guarantee of profitability**. Trading in financial markets carries a risk of capital loss. Use of this tool is entirely at the user's own risk. The developer accepts no responsibility for any losses incurred.

### 📜 License

This project is released under a proprietary license. See the [LICENSE](LICENSE) file for details.

### 📞 Contact

- **Telegram:** [@Darknighte5a](https://t.me/Darknighte5a)

###Donate ME

BTC Wallet: bc1ql6fwvu4dwsv32fs9tkh454y8hrd0gs6esaade24t9hexwnnq6lkskarqkf

Lightning Wallet: lnbc1p49jdtdpp52d82np6sy49mqgpmy3dmuhk5cfxjlm9sywsfrlralg57fqv42c6qdqqcqzzgxqyz5vqrzjqf0wu22xsefd8gzu0m9n93g2khea86l6yy26en9v46g9e6hk7v9z8m287z05kagmsuqqqqryqqqqthqqpyrzjqfwdd2w9y5ra5z3m4qetfa5ccu6432xfuvk6zrvg9vxwltvukd48dm287z05kagmsuqqqqryqqqqthqqpysp5sxtsp3gmh8rnk3c7hsynqsuq20tnhhv470200tjnk8rnc3q6akls9qrsgqegmhm5w9f2dkdyr6jkltzujqnq3xh2gclt3psmxuk5h7x47mpe63fm9q4533xm6822fm3h59567gmyjah0vynzygpkmsksnhqg0wn2gp383jfc

Eth and BNB wallet: 0x2C2f11eF7203D66fEb4c4f594F9f3a2A40394f3e

TRX Wallet: TDzq7z4ZkQTsAAzRxy1JXKJ985HRhAMKsD
---

<div align="center">

**© 2026 Darknighte5a — All Rights Reserved**

</div>
