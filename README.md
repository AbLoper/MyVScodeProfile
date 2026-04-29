# 🧰 VS Code Setup Guide

> دليل سريع واحترافي لإعداد بيئة **Visual Studio Code** خلال دقائق 🚀

---

## 📌 Overview

هذا الدليل يساعدك على:

* تثبيت جميع الإضافات (Extensions) دفعة واحدة
* تطبيق إعداداتك المخصصة بسهولة
* توحيد بيئة العمل بين الأجهزة

---

## ⚡ Requirements

تأكد من توفر التالي قبل البدء:

* تثبيت **VS Code**
* إضافة الأمر `code` إلى الـ PATH
  *(يمكن تفعيله من داخل VS Code عبر: Command Palette → `Shell Command: Install 'code' command in PATH`)*

---

## 📦 Install Extensions

### 🟢 الطريقة 1: من النظام الحالي

تثبيت نفس الإضافات الموجودة لديك:

```powershell
code --list-extensions | ForEach-Object { code --install-extension $_ }
```

// في حال لم يعمل الأمر code استخدم الأمر code.cmd

---

### 🔵 الطريقة 2: من ملف

إذا كان لديك ملف `extensions.txt`:

```powershell
Get-Content extensions.txt | ForEach-Object { code --install-extension $_ }
```

---

## ⚙️ Apply Settings

قم بنسخ ملفات الإعدادات إلى المسار المناسب لنظامك:

| النظام     | المسار                                    |
| ---------- | ----------------------------------------- |
| 🪟 Windows | `%APPDATA%\Code\User`                     |
| 🍎 macOS   | `~/Library/Application Support/Code/User` |
| 🐧 Linux   | `~/.config/Code/User`                     |

### 📁 الملفات المطلوبة:

```text
settings.json
keybindings.json
```

---

## 🔄 Restart

بعد الانتهاء من جميع الخطوات:

```bash
# فقط أغلق VS Code وأعد تشغيله
```

---

## 💡 Tips

* احتفظ بملف `extensions.txt` محدث دائمًا
* استخدم Git لمزامنة إعداداتك بين الأجهزة
* يمكنك إضافة ملفات أخرى مثل:

  * `snippets`
  * `tasks.json`
  * `launch.json`

---

## 📎 Example Project Structure

```text
vscode-setup/
│
├── extensions.txt
├── settings.json
├── keybindings.json
└── README.md
```

---

## 🏁 Done!

🎉 الآن بيئة VS Code الخاصة بك جاهزة للاستخدام على أي جهاز.

إذا أردت نسخة تدعم **dotfiles + مزامنة تلقائية + GitHub Actions** أخبرني وسأجهزها لك.
