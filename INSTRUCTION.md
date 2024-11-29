[English](#english) | [Русский](#russian)

---

<a name="english"></a>
# English Version 

## 📋 Table of Contents
1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Using the Bot](#using-the-bot)
4. [Initial Setup](#initial-setup)
5. [Account Configuration](#account-configuration)
6. [Troubleshooting](#troubleshooting)
7. [Proxy Setup](#proxy-setup)
8. [Configuration Setup](#configuration-setup)

## 💻 Requirements
- Minimum 4GB RAM
- Capsolver api token
- Ready accounts or mails for registration
- Proxies
- Stable internet connection

## 🔧 Installation with start.sh (Linux)
1. Download the bot from the official source
2. Unzip the files to your preferred location
3. Updating system + install Node.js: 
`sudo apt update`
`sudo apt upgrade`
`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`
`sudo apt-get install -y nodejs`,`chmod +x start.sh`
`bash start.sh`
4. Install Node.js 
5. Run the setup file (start.sh) to install dependencies and run bot

## 🔧 Installation with start.bat (Windows)
1. Download the bot from the official source
2. Unzip the files to your preferred location
3. Install Node.js - https://nodejs.org/en/download/package-manager

4. Run the setup file (start.bat) to install dependencies and run bot
![Launch](https://i.imgur.com/BVnO8yg.gif)

### Configuration Setup
The `config.js` file contains important settings for the bot. Here are the key sections you might want to configure:

1. **Registration Settings**
```javascript
FEATURES_CONFIG.REGISTRATION = {
    APPROVE_EMAIL: true,          // Email confirmation
    CONNECT_WALLET: true,         // Wallet connection
    REF_CODES: [                  // Your referral codes
        "mrcb4ojX7Wbxwv0"
    ],
}
```

2. **Captcha Settings**
```javascript
FEATURES_CONFIG.CAPTCHA = {
    CAPSOLVER_API_KEY: '',        // Your Capsolver API key
}
```

3. **Night Mode Settings**
```javascript
FEATURES_CONFIG.NIGHT_MODE = {
    ENABLED: false,               // Enable/disable night mode
    START_HOUR: 23,              // Start hour (23:00)
    END_HOUR: 6,                 // End hour (06:00)
    RECONNECT_SPREAD: {
        MIN_MINUTES: 30,         // Minimum reconnection time
        MAX_MINUTES: 120         // Maximum reconnection time
    }
}
```

4. **Telegram Notifications** (Optional)
```javascript
FEATURES_CONFIG.TELEGRAM = {
    ENABLED: false,              // Enable/disable Telegram bot
    BOT_TOKEN: '',              // Your Telegram bot token
    CHAT_ID: '',                // Your chat ID
    UPDATE_INTERVAL: 5000,      // Message update interval (5 seconds)
}
```

## 🚀 Using the Bot

### Functions
1. ➕ Create New Account (Manual adding account)
2. ✏️ Edit Account (Manual editing account with switch connectionType or add proxy)
3. 🗑️ Delete Account (Manual deleting account from accounts.json)
4. 🌿 Start Farm 
5. 📝 Register New Account (Automatic registration ∞ accounts with referral link support)

## ⚙️ Initial Setup
1. If you already have accounts, go to [Account Configuration](#account-configuration), if not, proceed to registration [Account Register](#account-register)
2. Run the setup file (start.bat) / (start.sh)
3. Click Start Farm

![Start Farm - Demonstration of starting the farming process](https://i.imgur.com/vxN40Gx.gif)

## 👤 Account Configuration

Account registration is fully automated, please upload your data to proxies.txt and emails.txt beforehand
![Account Registration - Shows the process of registering a new account](https://i.imgur.com/zFElQT7.gif)

Account editing:
1. Add / change proxy
2. Change farm type extension / desktop
![Account Editing - Demonstrates how to edit account settings](https://i.imgur.com/hytMvy6.gif)

### Setting Up Your Account
```json
[
  {
    "username": "your-email@example.com",
    "password": "password",
    "wallet": {
      "address": "your-wallet-address", // It is not necessary to specify for the launch of farm, it will appear during registration
      "privateKey": "your-wallet-private-key" // too
    },
    "proxies": [
      {
        "url": "http://login:password@ip:port", //socks5
        "userAgent": "your-user-agent", //generated automatically
        "connectionType": "extension" // or "desktop"
      }
    ],
    "enabled": true // turn on or off account
  }
]
```

### Proxy Setup
- Supported formats:
  - HTTP/HTTPS
  - SOCKS5
- Required format: 
`schema://user:pass@ip:port`
`schema://ip:port@user:pass`
`schema://user:pass:ip:port`
`schema://ip:port:user:pass`

### Starting the Farm
Before starting the farm, make sure you have loaded all the data in accounts.json, the format is specified in the instructions
![Starting the Farm - Farm launch](https://i.imgur.com/vxN40Gx.gif)

## ❓ Troubleshooting
- Common issues and solutions (in process)
- Support contacts (@Diveroli_AEY)

---

<a name="russian"></a>
# Русская Версия

## 📋 Содержание
1. [Требования](#требования)
2. [Установка](#установка)
3. [Использование бота](#использование-бота)
4. [Начальная настройка](#начальная-настройка)
5. [Настройка аккаунта](#настройка-аккаунта)
6. [Решение проблем](#решение-проблем)
7. [Настройка прокси](#настройка-прокси)
8. [Настройка конфигурации](#настройка-конфигурации)

## 💻 Требования
- Минимум 4 ГБ оперативной памяти
- Capsolver api token
- Готовые аккаунты или почты для регистрации
- Прокси
- Стабильное интернет-соединение

## 🔧 Установка с помощью start.sh (Linux)
1. Скачайте бота из официального источника
2. Распакуйте файлы в удобное для вас место
3. Обновление системы + установка Node.js:
`sudo apt update`
`sudo apt upgrade`
`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`
`sudo apt-get install -y nodejs`,`chmod +x start.sh`
`bash start.sh`
4. Установите Node.js
5. Запустите установочный файл (start.sh) для установки зависимостей и запуска бота

## 🔧 Установка с помощью start.bat (Windows)
1. Скачайте бота из официального источника
2. Распакуйте файлы в удобное для вас место
3. Установите Node.js - https://nodejs.org/en/download/package-manager

4. Запустите установочный файл (start.bat) для установки зависимостей и запуска бота
![Запуск](https://i.imgur.com/BVnO8yg.gif)

### Настройка конфигурации
Файл `config.js` содержит важные настройки для бота. Вот основные разделы, которые вы можете настроить:

1. **Настройки регистрации**
```javascript
FEATURES_CONFIG.REGISTRATION = {
    APPROVE_EMAIL: true,          // Подтверждение email
    CONNECT_WALLET: true,         // Подключение кошелька
    REF_CODES: [                  // Ваши реферальные коды
        "mrcb4ojX7Wbxwv0"
    ],
}
```

2. **Настройки капчи**
```javascript
FEATURES_CONFIG.CAPTCHA = {
    CAPSOLVER_API_KEY: '',        // Ваш API ключ от Capsolver
}
```

3. **Настройки ночного режима**
```javascript
FEATURES_CONFIG.NIGHT_MODE = {
    ENABLED: false,               // Включение/выключение ночного режима
    START_HOUR: 23,              // Час начала (23:00)
    END_HOUR: 6,                 // Час окончания (06:00)
    RECONNECT_SPREAD: {
        MIN_MINUTES: 30,         // Минимальное время до переподключения
        MAX_MINUTES: 120         // Максимальное время до переподключения
    }
}
```

4. **Уведомления в Telegram** (Опционально)
```javascript
FEATURES_CONFIG.TELEGRAM = {
    ENABLED: false,              // Включение/выключение Telegram бота
    BOT_TOKEN: '',              // Ваш токен бота Telegram
    CHAT_ID: '',                // Ваш ID чата
    UPDATE_INTERVAL: 5000,      // Интервал обновления сообщений (5 секунд)
}
```

## 🚀 Использование бота

### Функции
1. ➕ Create New Account (Ручное добавление аккаунта)
2. ✏️ Edit Account (Ручное редактирование аккаунта с переключением типа подключения или добавлением прокси)
3. 🗑️ Delete Account (Ручное удаление аккаунта из accounts.json)
4. 🌿 Start Farm 
5. 📝 Register New Account (Автоматическая регистрация ∞ аккаунтов с поддержкой реферальных ссылок)

## ⚙️ Начальная настройка
1. Если у вас уже есть аккаунты, перейдите к [Настройка аккаунта](#настройка-аккаунта), если нет, перейдите к регистрации [Регистрация аккаунта](#регистрация-аккаунта)
2. Запустите файл настройки (start.bat) / (start.sh)
3. Нажмите Start Farm

![Start Farm - Демонстрация процесса запуска фарминга](https://i.imgur.com/vxN40Gx.gif)

## 👤 Настройка аккаунта

Регистрация аккаунта полностю автоматизирована, предварительно загрузите данные в proxies.txt и emails.txt
![Регистрация аккаунта - Показывает процесс регистрации нового аккаунта](https://i.imgur.com/zFElQT7.gif)

Редактирование аккаунта:
1. Добавление / изменение прокси 
2. Смена типа фарма extension / desktop
![Редактирование аккаунта - Демонстрирует как редактировать настройки аккаунта](https://i.imgur.com/hytMvy6.gif)

### Настройка вашего аккаунта
```json
[
  {
    "username": "ваш-email@example.com",
    "password": "пароль",
    "wallet": {
      "address": "адрес-вашего-кошелька", // Не обязательно указывать для запуска фарма, появится при регистрации
      "privateKey": "приватный-ключ-кошелька" // тоже
    },
    "proxies": [
      {
        "url": "http://логин:пароль@ip:порт", //socks5
        "userAgent": "user-agent", //генерируется автоматически
        "connectionType": "extension" // или "desktop"
      }
    ],
    "enabled": true // включить или выключить аккаунт
  }
]
```

### Настройка прокси
- Поддерживаемые форматы:
  - HTTP/HTTPS
  - SOCKS5
- Требуемый формат: 
`schema://user:pass@ip:port`
`schema://ip:port@user:pass`
`schema://user:pass:ip:port`
`schema://ip:port:user:pass`


### Запуск фарма
Перед запуском фарма убедитесь, что в accounts.json вы загрузили все данные, формат указан в инструкции
![Запуск фарма - Запуск фарма](https://i.imgur.com/vxN40Gx.gif)
## ❓ Решение проблем
- Частые проблемы и их решения (в процессе)
- Контакты поддержки (@Diveroli_AEY)

---
