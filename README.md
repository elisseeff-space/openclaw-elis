# openclaw-elis
openclaw-elis

ssh -N -L 18789:127.0.0.1:18789 -p 13131 pavel@docs.kkdessin.ru
ssh -N -L 18789:127.0.0.1:18789 pavel@claw.elisseeff.ru


# Добавляем модели Yandex 
Отлично! Нашёл статью о добавлении кастомных провайдеров. Давайте посмотрим детали:
- https://haimaker.ai/blog/integrating-custom-llm-providers-with-clawdbot/  

Что сделано:

     1. Добавлен провайдер Yandex в ~/.openclaw/openclaw.json
     2. Две модели доступны:
        - yandex/yandexgpt/latest (alias: YandexGPT) — Pro версия
        - yandex/yandexgpt-lite/latest (alias: YandexGPT-Lite) — Lite версия

    Использование:

    Переключение на YandexGPT:

     1 openclaw models set "yandex/yandexgpt-lite/latest"

    Или через alias:

     1 openclaw models set "YandexGPT-Lite"

    Просмотр доступных моделей:

     1 openclaw models list

    Тест прошёл успешно — YandexGPT отвечает на запросы.

Переключение между моделями:

     1 # На YandexGPT Lite
     2 openclaw models set "YandexGPT-Lite"
     3 
     4 # На YandexGPT Pro
     5 openclaw models set "YandexGPT"
     6 
     7 # На OpenRouter (Claude)
     8 openclaw models set "openrouter/anthropic/claude-sonnet-4.5"

    Просмотр текущего статуса:

     1 openclaw models status
