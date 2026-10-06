# Rus12325

Профиль — витрина проектов. ESP32-прошивки, CYD-хардвар, HMI-локализация, AI-ассистенты, CAD-генераторы и ноутбуки Klipper.

![GitHub followers](https://img.shields.io/github/followers/Rus12325?label=Followers&style=flat-square&color=58a6ff)
![GitHub repos](https://img.shields.io/github/repo-stats/repos/?username=Rus12325&layout=flat&theme=github-light&color=58a6ff&combine=PRs_Issues_Stars&show_count=true&label=Repos)
![GitHub language count](https://img.shields.io/github/languages/count/Rus12325/Rus12325?label=Languages&style=flat-square&color=58a6ff)
![GitHub top language](https://img.shields.io/github/languages/top/Rus12325/Rus12325?label=Top%20language&style=flat-square&color=58a6ff)

---

## 🧭 Навигация

- **[ESP32 / встроенное ПО](#esp32--встроенное-по)** — прошивки для CYD, S3/C6, интернет-радио и дашборды железа.
  - [Голосовые ассистенты](#голосовые-ассистенты)
  - [Интернет-радио и дашборды ПК](#интернет-радио-и-дашборды-пк)
  - [Matter / Zigbee / реле](#matter--zigbee--реле)
- **[CYD: корпуса и органы](#cyd-корпуса-и-органы)** — CAD-модели, Front Panel, STL.
- **[Klipper на CYD](#klipper-на-cyd)** — ноутбуки, скрипты прошивки, мок Moonraker.
- **[AI-ассистенты в вебе](#ai-ассистенты-в-вебе)** — веб-ассистенты на Groq и Replicate.
- **[HMI-локализация и патч строк](#hmi-локализация-и-патч-строк)** — три проекта в связке для Windows-HMI.
- **[Стартовые репозитории](#стартовые-репозитории)** — что брать первым.

---

## ESP32 / встроенное ПО

Прошивки для ESP32-семейства: в основном Cheap Yellow Display (CYD) и варианты S3/C6, на PlatformIO и ESP-IDF/Matter там, где это имеет смысл. Голос, звук, мониторинг железа, умный домашний контроль — всё, что можно утащить на микроконтроллер.

---

<details>
<summary><b>Голосовые ассистенты</b></summary>

| Проект | Технологии | Что это |
|---|---|---|
| **[esp32-s3-ai-assistant-yandex](https://github.com/Rus12325/esp32-s3-ai-assistant-yandex)** | `C++` · PlatformIO | Голосовой ассистент ESP32-S3: распознавание и синтез речи Yandex SpeechKit, YandexGPT и слово активации. |
| **[esp32-s3-voice-assistant](https://github.com/Rus12325/esp32-s3-voice-assistant)** | `C++` · PlatformIO | Кнопка → речь: петля с синтезом Yandex SpeechKit прямо на устройстве. |
| **[esp32-gigachat-voice-assistant](https://github.com/Rus12325/esp32-gigachat-voice-assistant)** | `C++` · PlatformIO | Whisper-распознавание, GigaChat-ответы, дисплей ST7789. |

</details>

---

<details>
<summary><b>Интернет-радио и дашборды ПК</b></summary>

| Проект | Технологии | Что это |
|---|---|---|
| **[esp32-s3-internet-radio](https://github.com/Rus12325/esp32-s3-internet-radio)** | `C++` · PlatformIO | Интернет-радио ESP32-S3: MP3/AAC-потоки через усилитель MAX98357A, полностью статический аудио-тракт. |
| **[cyd-pc-monitor](https://github.com/Rus12325/cyd-pc-monitor)** | `Python` · PlatformIO | Дашборд железа ПК на ESP32-2432S028 CYD: прошивка, хост-приложение и последовательный протокол. |
| **[esp32-pc-monitor-lvgl](https://github.com/Rus12325/esp32-pc-monitor-lvgl)** | `C` · PlatformIO | Монитор ПК на CYD с LVGL, таблицами кириллических шрифтов и Windows-агентом телеметрии. |

</details>

---

<details>
<summary><b>Matter / Zigbee / реле</b></summary>

| Проект | Технологии | Что это |
|---|---|---|
| **[matter-relay](https://github.com/Rus12325/matter-relay)** | `C++` · ESP-Matter | Реле на ESP32-C6: импульсный канал для кнопки включения ПК и удерживающее реле, сохранённое в NVS. |
| **[esp32c6-zigbee-relay](https://github.com/Rus12325/esp32c6-zigbee-relay)** | `C++` · PlatformIO | Известная рабочая конфигурация PlatformIO для сборки Zigbee-прошивки на ESP32-C6 в рамках Arduino-фреймворка. |

</details>

---

## CYD: корпуса и органы

Работа с корпусом и органами CYD-терминалов: CAD-моделирование, Front Panel в браузере, генерация STL. Здесь проекты ближе к дизайну и вёрстке, чем к микроконтроллерному коду.

| Проект | Технологии | Что это |
|---|---|---|
| **[cyd-2432s028-case](https://github.com/Rus12325/cyd-2432s028-case)** | `Python` · FreeCAD | Бесголовый генератор корпусов для ESP32 CYD: параметрические модели, проверенные STL для печати. |
| **[cyd-amplifier-front-panel](https://github.com/Rus12325/cyd-amplifier-front-panel)** | `HTML` · PlatformIO | Фронт-панель CYD для 5.1-усилителя: 24 В, реле глушения, спектр звука, сенсорный интерфейс, схемы подключения. |

---

## Klipper на CYD

Эксперименты по запуску станка с Klipper на CYD-доске (ESP32-2432S028 2USB). Заметки, скрипты прошивки, мок-раннинг Moonraker.

| Проект | Технологии | Что это |
|---|---|---|
| **[cyd-klipper-panel](https://github.com/Rus12325/cyd-klipper-panel)** | `Python` · PlatformIO | Заметки, скрипты прошивки и мок- harness Moonraker для запуска CYD-Klipper на ESP32-2432S028 2USB. |

---

## AI-ассистенты в вебе

AI-ассистенты рядом с железом: Node-бэкенды, обращающиеся к Groq и Replicate, с фронтендом на HTML/Markdown.

| Проект | Технологии | Что это |
|---|---|---|
| **[groq-replicate-ai-assistant](https://github.com/Rus12325/groq-replicate-ai-assistant)** | `HTML` · Node | Веб-ассистент, который параллельно опрашивает несколько Groq-моделей и генерирует изображения через Replicate. |

---

## HMI-локализация и патч строк

Целый слой инструментов для локализации и патча управляемых HMI-приложений Windows. Выцепляет строки, переводит, патчит сборки на лету и в рантайме.

| Проект | Технологии | Что это |
|---|---|---|
| **[langpatcher](https://github.com/Rus12325/langpatcher)** | `C#` | Патчер на базе Mono.Cecil, впрыскивающий кэш переводов в управляемые сборки HMI. |
| **[HMIPatcher](https://github.com/Rus12325/HMIPatcher)** | `Python` / C# | Набор для извлечения, перевода и патча UI-строк управляемого Windows-HMI-приложения. |
| **[hmi-translator](https://github.com/Rus12325/hmi-translator)** | `C#` | Библиотека рантайм-перевода для патченных HMI-сборок: кэшированный поиск с фильтрацией по идентификатору виджета. |

---

## Стартовые репозитории

Если хочешь быстро утащить что-то рабочее — вот точки входа:

- **[esp32-s3-internet-radio](https://github.com/Rus12325/esp32-s3-internet-radio)** — если нужен интернет-радио на CYD/S3 с минимальным количеством магии.
- **[cyd-pc-monitor](https://github.com/Rus12325/cyd-pc-monitor)** — если нужен монитор железа ПК на CYD с хост-агентом.
- **[cyd-2432s028-case](https://github.com/Rus12325/cyd-2432s028-case)** — если нужен корпус под CYD, который можно настроить и напечатать.
- **[hmi-translator](https://github.com/Rus12325/hmi-translator)** / **[HMIPatcher](https://github.com/Rus12325/HMIPatcher)** — если нужно перевести управляемый HMI-интерфейс.

---

## Аккуратность кода

Все репозитории публичные, коммиты подписаны как `Rus12325`.

Секреты — Wi-Fi пароли, API-ключи, Groq/Replicate-токены — вынесены в `.env` / `secrets.h` и добавлены в `.gitignore`, с пример-файлами на месте. Реальные значения не коммитятся.

Пароль Wi-Fi и ключи Yandex / OpenWeatherMap / OpenRouter / GigaChat, которые долго лежали в открытом виде на диске, в коде уже не фигурируют. Тем не менее — **рекомендуется сменить пароль Wi-Fi и перевыпустить ключи**.

---

## Профиль

- [github.com/Rus12325](https://github.com/Rus12325)

*Аккаунт: [github.com/Rus12325](https://github.com/Rus12325)*

![visitors](https://visitor-badge.laobi.icu/badge?page_id=Rus12325.Rus12325)
