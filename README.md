# 🚀 Pro Downloader

<div align="center">

**دانلودر حرفه‌ای فایل با GitHub Actions**

[![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF?logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![aria2](https://img.shields.io/badge/Downloader-aria2-orange)](https://aria2.github.io/)
![License](https://img.shields.io/badge/License-MIT-green)

<b>زبان:</b>  
🇮🇷 فارسی | <a href="#english">English</a>

</div>

---

# ⚠️ سلب مسئولیت (Disclaimer)

🚨 این پروژه صرفاً یک ابزار فنی برای مدیریت و خودکارسازی دانلود فایل‌ها با استفاده از GitHub Actions می‌باشد.

استفاده از این ابزار کاملاً بر عهده کاربر است.

## ❗ مسئولیت کاربر

با استفاده از این پروژه شما تأیید می‌کنید که:

- ✅ فقط فایل‌هایی را دانلود می‌کنید که اجازه قانونی دانلود و استفاده از آن‌ها را دارید.
- ✅ مالک محتوا هستید یا مجوز رسمی از صاحب اثر دارید.
- ✅ از این ابزار برای نقض کپی‌رایت، قوانین محلی یا بین‌المللی استفاده نخواهید کرد.
- ✅ از این ابزار برای دانلود محتوای غیرقانونی، مخرب یا ناقض قوانین GitHub استفاده نخواهید کرد.
- ✅ از این پروژه برای سوءاستفاده از منابع GitHub Actions یا ایجاد بار غیرعادی روی سرورها استفاده نخواهید کرد.

## 🚫 موارد استفاده ممنوع

استفاده از این پروژه برای موارد زیر اکیداً ممنوع است:

- دانلود یا توزیع محتوای دارای حق نشر بدون مجوز
- دور زدن سیستم‌های پرداخت، DRM یا محدودیت‌های دسترسی
- میزبانی، ذخیره یا توزیع محتوای غیرقانونی
- استفاده به عنوان CDN، فایل هاستینگ عمومی یا سیستم میرور عمومی
- هرگونه فعالیتی که ناقض GitHub Terms of Service باشد

## 📜 انطباق با قوانین GitHub

این پروژه به‌گونه‌ای طراحی شده که صرفاً یک ابزار عمومی اتوماسیون باشد و هیچ سرویس میزبانی فایل عمومی ارائه نمی‌دهد.

کاربران موظف هستند:

- شرایط استفاده GitHub (GitHub Terms of Service)
- سیاست استفاده قابل قبول (Acceptable Use Policy)
- قوانین کپی‌رایت (DMCA)

را مطالعه و رعایت نمایند.

## ⚖️ محدودیت مسئولیت

نویسنده این پروژه:

- هیچ مسئولیتی در قبال نحوه استفاده کاربران ندارد.
- مسئولیتی در قبال محتوای دانلودشده ندارد.
- هیچ‌گونه ضمانتی در مورد قانونی بودن استفاده کاربران ارائه نمی‌دهد.

در صورت سوءاستفاده، مسئولیت کامل بر عهده کاربر نهایی خواهد بود.

---

با استفاده از این پروژه، شما تمامی شرایط فوق را می‌پذیرید.



<a name="persian"></a>

# 🇮🇷 راهنمای فارسی

## ✨ معرفی

یک ابزار قدرتمند مبتنی بر **GitHub Actions** است که می‌تواند فایل‌ها را به‌صورت خودکار دانلود کند، آن‌ها را بر اساس نوع دسته‌بندی کند و در صورت نیاز آن‌ها را فشرده‌سازی نماید.

این سیستم از **aria2** برای دانلود سریع با چند اتصال همزمان استفاده می‌کند.

---

## ⚡ ویژگی‌ها

- 🚀 دانلود فوق سریع با **aria2**
- 📂 دسته‌بندی خودکار فایل‌ها
- 🔐 امکان رمزگذاری فایل‌های فشرده
- ✂️ تقسیم فایل‌های بزرگ به چند بخش
- 🔁 ادامه دانلود در صورت قطع شدن
- 📊 تولید **SHA256 checksum**
- 🧾 ساخت فایل **metadata**
- 🎯 اجرای workflow به دو روش مختلف
- ⚙️ تنظیمات قابل شخصی‌سازی

---

## 🚀 نحوه استفاده

### روش اول — اجرای دستی (پیشنهادی)

1. وارد تب **Actions** در ریپازیتوری شوید
2. workflow با نام **Pro Downloader** را انتخاب کنید
3. روی **Run workflow** کلیک کنید
4. لینک‌های دانلود را وارد کنید

مثال:

```
https://example.com/file1.mp4
https://example.com/file2.zip
https://example.com/music.mp3
```
تنظیمات اختیاری:

**Archive format**


7z
zip
tar.gz
none

**Split size**


90m
500m
1g

**Password**


mypassword123

**Connections**


16

---

## ⚙️ روش دوم — اجرای دانلود با Commit

می‌توانید با یک commit ساده دانلود را اجرا کنید.

مثال:


```
download: https://example.com/file.zip
```

چند فایل:


```
download: https://site.com/a.mp4 https://site.com/b.mp3
```

دانلود و ساخت آرشیو ZIP:


```
download-zip: https://example.com/video.mp4
```

---

## 📁 ساختار خروجی

بعد از اجرای workflow فایل‌ها به شکل زیر مرتب می‌شوند:

```
downloads/
├── video/
├── audio/
├── image/
├── document/
├── archive/
├── other/
├── checksums.txt
└── metadata.json
```

توضیح پوشه‌ها:

- **video** → فایل‌های ویدیویی  
- **audio** → فایل‌های صوتی  
- **image** → تصاویر  
- **document** → PDF و فایل‌های متنی  
- **archive** → فایل‌های zip و rar  
- **other** → سایر فایل‌ها  

---

## 📋 مثال استفاده

نمونه تنظیمات workflow:


URLs:
https://example.com/movie.mp4
https://example.com/music.mp3

Archive format: 7z
Split size: 100m
Password: mypassword
Connections: 16

---

## 📜 لایسنس

MIT License — استفاده و تغییر آزاد است.

---

# ⚠️ Disclaimer

🚨 This project is a technical automation tool built on GitHub Actions for downloading and organizing files.

Use of this tool is entirely at your own risk.

## ❗ User Responsibility

By using this project, you agree that:

- ✅ You will only download content that you are legally permitted to access and use.
- ✅ You own the content or have proper authorization from the copyright holder.
- ✅ You will not use this tool to violate copyright laws or any local/international regulations.
- ✅ You will not use this project to download illegal, harmful, or policy‑violating content.
- ✅ You will not abuse GitHub Actions resources or generate excessive or abnormal traffic.

## 🚫 Prohibited Use

This project must NOT be used for:

- Downloading or distributing copyrighted material without permission
- Circumventing paywalls, DRM, or access control systems
- Hosting, storing, or distributing illegal content
- Operating as a public file hosting service, CDN, or mirror system
- Any activity that violates GitHub Terms of Service

## 📜 Compliance With GitHub Policies

This project is designed strictly as a generic automation workflow and does not provide any public hosting service.

Users are responsible for complying with:

- GitHub Terms of Service
- GitHub Acceptable Use Policy
- Copyright laws (including DMCA)

## ⚖️ Limitation of Liability

The author of this project:

- Is not responsible for how users utilize this tool
- Has no control over downloaded content
- Provides no guarantee regarding legal compliance of user activities

Any misuse is solely the responsibility of the end user.

---

By using this project, you acknowledge and accept all terms above.


<a name="english"></a>

# 🇬🇧 English Guide

## ✨ Overview

**Pro Downloader** is a powerful **GitHub Actions workflow** that automatically downloads files, organizes them by type, and optionally compresses them.

It uses **aria2** for high‑speed parallel downloading.

---

## ⚡ Features

- 🚀 Ultra‑fast downloads using **aria2**
- 📂 Automatic file categorization
- 🔐 Optional archive password protection
- ✂️ Split large archives
- 🔁 Resume interrupted downloads
- 📊 Automatic **SHA256 checksums**
- 🧾 Metadata generation
- 🎯 Multiple workflow triggers
- ⚙️ Customizable configuration

---

## 🚀 How To Use

### Method 1 — Run Manually

1. Open the **Actions** tab in your repository
2. Select **Pro Downloader**
3. Click **Run workflow**
4. Enter download URLs

Example:

```
https://example.com/file1.mp4
https://example.com/file2.zip
```
Optional parameters:

Archive format:


7z
zip
tar.gz
none

Split size:


90m
500m
1g

Connections:


16

Password:


mypassword

---

## ⚙️ Method 2 — Trigger via Commit

Run downloads directly using commit messages.

Example:

```
download: https://example.com/file.zip
```
Multiple files:

```
download: https://site.com/a.mp4 https://site.com/b.mp3
```
Download and create ZIP archive:

```
download-zip: https://example.com/video.mp4
```
---

## 📁 Output Structure

```
downloads/
├── video/
├── audio/
├── image/
├── document/
├── archive/
├── other/
├── checksums.txt
└── metadata.json
```
Description:

- **video** → video files  
- **audio** → audio files  
- **image** → images  
- **document** → documents  
- **archive** → compressed files  

---

## 📜 License

MIT License
