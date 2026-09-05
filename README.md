# 💰 Финансовый трекер

Android-приложение для учёта доходов, расходов и накоплений. Все данные хранятся локально на устройстве — не нужен интернет, регистрация или сервер.

![Platform](https://img.shields.io/badge/platform-Android-3DDC84?logo=android)
![Kotlin](https://img.shields.io/badge/kotlin-2.2.10-7F52FF?logo=kotlin)
![API](https://img.shields.io/badge/minSDK-24+-blue?logo=android)
![License](https://img.shields.io/badge/license-MIT-green)

## 📸 Скриншоты

| Главная | Транзакции | Графики | Цели |
|---|---|---|---|
| Обзор баланса | Список операций | Расходы по категориям | Прогресс накоплений |

## ✨ Функции

- **💸 Доходы и расходы** — добавление транзакций по категориям с описанием и датой
- **🎯 Цели накоплений** — создание целей, внесение/снятие средств, прогресс-бары
- **📊 Графики** — расходы по категориям, доходы по категориям, динамика за 30 дней
- **🔍 Фильтрация** — по типу (доход/расход) и по категории
- **📴 Оффлайн** — все данные хранятся в localStorage на устройстве
- **🎨 Тёмная тема** — Material Design 3, оптимизировано для мобильных

## 📱 Категории

| Расходы | Доходы |
|---|---|
| 🛒 Продукты | 💼 Зарплата |
| 🚗 Транспорт | 💻 Фриланс |
| 🏠 Жильё | 📈 Инвестиции |
| 🎮 Развлечения | 🎁 Подарок |
| 👕 Одежда | 💳 Кэшбэк |
| 💊 Здоровье | ↩️ Возврат |
| 📚 Образование | 📦 Другое |
| 📱 Связь | |
| 🍽️ Рестораны | |
| 📺 Подписки | |
| 📦 Другое | |

## 🛠️ Технологии

- **Язык:** Kotlin
- **UI:** WebView + HTML/CSS/JavaScript
- **Хранение:** localStorage (встроен в WebView)
- **Сборка:** Gradle 9.4.1 + AGP 9.2.0
- **Min SDK:** 24 (Android 7.0+)
- **Target SDK:** 36

## 🚀 Сборка APK

### Требования

- [Android Studio](https://developer.android.com/studio) (или JDK 17+ и Android SDK)
- Android SDK: `compileSdk 36`, `build-tools 36.0.0+`
- Gradle 9.4.1 (включён в `gradle/wrapper`)

### Клонирование

```bash
git clone https://github.com/NIRAqwerty/draft_proposal12.git
cd draft_proposal12
```

### Сборка

```bash
# Debug APK
./gradlew assembleDebug

# Release APK
./gradlew assembleRelease
```

APK будет в:
```
app/build/outputs/apk/debug/app-debug.apk
app/build/outputs/apk/release/app-release.apk
```

### Через Android Studio

1. Откройте проект в Android Studio
2. Нажмите **Build → Build Bundle(s) / APK(s) → Build APK(s)**
3. APK появится в `app/build/outputs/apk/debug/`

## 📲 Установка на телефон

1. Скопируйте `app-debug.apk` на телефон (USB, Google Drive, мессенджер)
2. Откройте файл на телефоне
3. Разрешите установку из неизвестных источников
4. Нажмите **Установить**
5. Готово — приложение «Финансовый трекер» на рабочем столе!

## 📁 Структура проекта

```
app/src/main/
├── assets/
│   ├── index.html          # Основное приложение (HTML/CSS/JS)
│   ├── manifest.json       # PWA манифест
│   ├── sw.js               # Service Worker (офлайн)
│   └── icons/              # Иконки приложения
├── java/com/financetracker/app/
│   └── MainActivity.kt     # Android Activity с WebView
├── res/
│   ├── mipmap-*/           # Иконки запуска
│   └── values/strings.xml  # Строки и тема
└── AndroidManifest.xml     # Манифест Android

gradle/
├── libs.versions.toml      # Версии зависимостей
└── wrapper/                # Gradle wrapper
```

## 📄 Лицензия

MIT License — используйте свободно.
