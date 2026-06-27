# 🚀 FluentFlash

![Version](https://img.shields.io/badge/version-1.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Platform](https://img.shields.io/badge/platform-Linux-lightgrey)
![Python](https://img.shields.io/badge/Python-3.12%2B-blue)

**Создание загрузочных USB-накопителей для Linux**  
*Простой и минималистичное приложения для создание загрузочных накопителей *

---

## 📦 Что это?

FluentFlash — это графическая утилита для записи ISO-образов на USB-флешки.  
Она создана для Linux и поддерживает все основные функции:

- ✅ Запись любых ISO (Linux, Windows, BSD и др.)
- ✅ Автоопределение типа загрузки (Legacy / UEFI / Hybrid)
- ✅ Создание таблиц разделов (MBR / GPT)
- ✅ Проверка хешей (MD5, SHA1, SHA256)
- ✅ Изменение метки тома (FAT32, NTFS, exFAT, ext4, UFS)
- ✅ Подробный лог операций (как в Rufus)
- ✅ Тёмная тема
- ✅ Работает без установки

---

## 📥 Скачать

[Скачать последнюю версию](https://github.com/winintern/FluentFlash/releases/download/V1.0/FluentFlash-1.0-x86_64.AppImage)  
Файл: `FluentFlash-1.0-x86_64.AppImage`

---

## ⚡ Быстрый старт

### 1. Сделайте файл исполняемым

```bash
chmod +x FluentFlash-1.0-x86_64.AppImage
sudo ./FluentFlash-1.0-x86_64.AppImage
Почему нужен sudo?
Программа работает напрямую с USB-устройствами (/dev/sdX), создаёт разделы и записывает образы.
В Linux доступ к блочным устройствам есть только у root. Это стандартная практика для всех аналогичных утили
🖥️ Системные требования
Linux

Python 3.12+ (для сборки из исходников)

100 MB свободного места

📋 Зависимости
sudo pacman -S pv parted gdisk dosfstools ntfs-3g exfatprogs e2fsprogs libisoburn cdrtools
Для других дистрибутивов — аналоги:

Debian/Ubuntu: apt install pv parted gdisk dosfstools ntfs-3g exfatprogs e2fsprogs xorriso

Fedora: dnf install pv parted gdisk dosfstools ntfs-3g exfatprogs e2fsprogs xorris
🔧 Возможности
Функция	Описание
Выбор ISO	Поддерживаются образы Linux, Windows, BSD
Выбор USB	Автоопределение всех подключённых флешек
Схема разделов	MBR (Legacy) / GPT (UEFI) / Авто
Файловая система	FAT32, NTFS, exFAT, ext4, UFS
Метка тома	Авто или вручную
Проверка хеша	MD5, SHA1, SHA256 после записи
Логирование	Подробный лог, как в Rufus
Тёмная тема	Комфортная работа в любом освещении

🛠️ Сборка из исходников
bash
git clone https://github.com/winitern/fluentflash
cd fluentflash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
pyinstaller --onefile --windowed --hidden-import PySide6.QtCore --hidden-import PySide6.QtGui --hidden-import PySide6.QtWidgets --name FluentFlash fluentflash.py
После сборки бинарник будет в dist/FluentFlash.

📝 Лицензия
MIT License — свободное использование, модификация, распространение.

🙏 Благодарность
Иконка USB от Freepik на Flaticon

Автор: winitern
GitHub: github.com/winitern

Сделано с ❤️ для Linux-сообщества
