# Rus12325 / 작업 / Projects

Профиль — витрина опубликованных проектов. У каждого — свой домен, свой стек, одна общая тема: заставить железо и софт работать вместе без лишней магии.

---

## 🧭 Contents

- [ESP32 / embedded firmware](#esp32--embedded-firmware)
  - [Voice assistants](#voice-assistants)
  - [Internet radio & PC dashboards](#internet-radio--pc-dashboards)
  - [Matter / Zigbee / relay logic](#matter--zigbee--relay-logic)
- [CYD case & front-panel tooling](#cyd-case--front-panel-tooling)
- [Klipper on a CYD](#klipper-on-a-cyd)
- [AI web assistants](#ai-web-assistants)
- [HMI localization & string patching](#hmi-localization--string-patching)
- [Upstream reference fork](#upstream-reference-fork)

---

## ESP32 / embedded firmware

Firmware for ESP32-family boards, mostly Cheap Yellow Display (CYD) and S3/C6 variants, built on PlatformIO and ESP-IDF/Matter where it makes sense. Голос, звук, мониторинг железа, умный домашний контроль — всё, что можно притащить на микроконтроллер.

### Voice assistants

| Project | Stack | What it does |
|---|---|---|
| [esp32-s3-ai-assistant-yandex](https://github.com/Rus12325/esp32-s3-ai-assistant-yandex) | `C++` / PlatformIO | ESP32-S3 voice assistant: Yandex SpeechKit speech recognition and TTS with YandexGPT and a wake word. |
| [esp32-s3-voice-assistant](https://github.com/Rus12325/esp32-s3-voice-assistant) | `C++` / PlatformIO | ESP32-S3 voice assistant: button-to-speech loop with Yandex SpeechKit TTS synthesized on-device. |
| [esp32-gigachat-voice-assistant](https://github.com/Rus12325/esp32-gigachat-voice-assistant) | `C++` / PlatformIO | ESP32 voice assistant with Whisper speech recognition, GigaChat replies and an ST7789 display. |

### Internet radio & PC dashboards

| Project | Stack | What it does |
|---|---|---|
| [esp32-s3-internet-radio](https://github.com/Rus12325/esp32-s3-internet-radio) | `C++` / PlatformIO | ESP32-S3 internet radio: MP3/AAC streams through a MAX98357A amplifier with a fully static audio pipeline. |
| [cyd-pc-monitor](https://github.com/Rus12325/cyd-pc-monitor) | `Python` / PlatformIO | PC hardware dashboard on an ESP32-2432S028 CYD: firmware, host application and serial protocol. |
| [esp32-pc-monitor-lvgl](https://github.com/Rus12325/esp32-pc-monitor-lvgl) | `C` / PlatformIO | ESP32 CYD PC monitor with LVGL, Cyrillic font tables and a Windows telemetry agent. |

### Matter / Zigbee / relay logic

| Project | Stack | What it does |
|---|---|---|
| [matter-relay](https://github.com/Rus12325/matter-relay) | `C++` / ESP-Matter | ESP32-C6 Matter relay with a momentary channel for a PC power button and a latching relay persisted in NVS. |
| [esp32c6-zigbee-relay](https://github.com/Rus12325/esp32c6-zigbee-relay) | `C++` / PlatformIO | Known-good PlatformIO configuration for building Zigbee firmware on the ESP32-C6 with the Arduino framework. |

---

## CYD case & front-panel tooling

Работа с корпусом и органами CYD-терминалов: CAD-моделирование, Front Panel в браузере, генерация STL. Здесь проекты ближе к дизайну и вёрстке, чем к микроконтроллерному коду.

| Project | Stack | What it does |
|---|---|---|
| [cyd-2432s028-case](https://github.com/Rus12325/cyd-2432s028-case) | `Python` / FreeCAD | Headless FreeCAD generator for parametric ESP32 CYD enclosures, producing verified STL for 3D printing. |
| [cyd-amplifier-front-panel](https://github.com/Rus12325/cyd-amplifier-front-panel) | `HTML` / PlatformIO | ESP32 CYD front panel for a 5.1 amplifier: 24V rail and mute control, audio spectrum, touch UI and wiring docs. |

---

## Klipper on a CYD

Эксперименты по запуску Klipper-машины на CYD-доске (ESP32-2432S028 2USB). Notes, scripted flashing, mock Moonraker-раннинг.

| Project | Stack | What it does |
|---|---|---|
| [cyd-klipper-panel](https://github.com/Rus12325/cyd-klipper-panel) | `Python` / PlatformIO | Notes, scripted flashing and a mock Moonraker harness for running CYD-Klipper on the ESP32-2432S028 2USB board. |

---

## AI web assistants

Веб-ассистенты рядом с железом: Node-бэкенды, обращающиеся к Groq и Replicate, с фронтендом на HTML/Markdown.

| Project | Stack | What it does |
|---|---|---|
| [groq-replicate-ai-assistant](https://github.com/Rus12325/groq-replicate-ai-assistant) | `HTML` / Node | Web assistant that queries several Groq models in parallel and generates images through Replicate. |

---

## HMI localization & string patching

Целыйслой инструментов для локализации и патча управляемых HMI-приложений Windows. Выцепляет строки, переводит, патчит сборки на лету и в рантайме.

| Project | Stack | What it does |
|---|---|---|
| [langpatcher](https://github.com/Rus12325/langpatcher) | `C#` | Mono.Cecil-based patcher that injects a runtime translation cache into managed HMI assemblies. |
| [HMIPatcher](https://github.com/Rus12325/HMIPatcher) | `Python` / C# | Toolkit to extract, translate and patch the UI strings of a managed Windows HMI application. |
| [hmi-translator](https://github.com/Rus12325/hmi-translator) | `C#` | Runtime translation library for patched HMI assemblies: cached table lookup with widget-identifier filtering. |

---

## Upstream reference fork

| Project | Stack | What it does |
|---|---|---|
| [CYM](https://github.com/Rus12325/CYM) | `C` / ESP-IDF | NerdMiner NM-CYD-C5 with TFT SPI 2.8" touch screen with diverse highly functional firmware. (Fork of upstream — [jimgat.github.io/CYM](https://jimgat.github.io/CYM/).) |

> Fork изначально залит как рабочий референс апстрима. Не претендует на авторство оригинального CYM-проекта.

---

### Binding / рубрикация

Все репозитории публичные, коммиты подписаны как `Rus12325`. Прошивки ESP32 выверены локальной сборкой там, где стоит инструментарий; кейсы и фронт-панели — документация и модели.

Секреты (Wi-Fi пароли, API-ключи, Groq/Replicate токены) вынесены в `.env` / `secrets.h` и добавлены в `.gitignore`, с пример-файлами на месте. Реальные значения не коммитятся.

---

*Аккаунт: [github.com/Rus12325](https://github.com/Rus12325)*
