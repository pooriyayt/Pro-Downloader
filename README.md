# 🚀 Pro Downloader

<div align="center">

**دانلودر حرفه‌ای فایل با GitHub Actions**

[![GitHub Actions](https://img.shields.io/badge/GitHub-Actions-2088FF?logo=github-actions&logoColor=white)](https://github.com/features/actions)
[![aria2](https://img.shields.io/badge/Downloader-aria2-orange)](https://aria2.github.io/)
[![License](https://img.shields.io/badge/License-MIT-green)]

<b>زبان:</b>  
🇮🇷 فارسی | <a href="#english">English</a>

</div>

---

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
