# Open-Source LLM Benchmarks & VRAM Requirements (2026) ⚡️

[![Telegram Channel](https://img.shields.io/badge/Telegram-@llm__hubs-2CA5E0?style=for-the-badge&logo=telegram)](https://t.me/llm_hubs)
[![WebApp Calculator](https://img.shields.io/badge/WebApp-VRAM%20Calculator-00d2ff?style=for-the-badge)](https://dangerousanen.github.io/llm-vram-calculator/)
[![GitHub Stars](https://img.shields.io/github/stars/DangerousANEN/awesome-llm-benchmarks-2026?style=for-the-badge)](https://github.com/DangerousANEN/awesome-llm-benchmarks-2026)

Сравнительная таблица производительности, скорости инференса (tok/s), реального потребления VRAM/RAM и формул KV-кэша для открытых SOTA моделей 2026 года: **DeepSeek R1, Qwen 3.8 / 2.5 Coder, GLM-5.2, Kimi K3, Llama 3.3**.

> 📢 **Официальный Telegram-канал проекта:**  
> Все обновления моделей, новые навыки, бенчмарки и инструменты сжатия контекста публикуются в канале **[.llm hubs (@llm_hubs)](https://t.me/llm_hubs)**.

---

## 🛠 Интерактивные Инструменты

- 🚀 **[Онлайн WebApp Калькулятор VRAM](https://dangerousanen.github.io/llm-vram-calculator/):** Динамический расчет памяти под веса + KV-кэш (MHA, GQA, MLA) до 128K контекста с подбором видеокарты.
- 📖 **[Архитектура VRAM: почему падают локальные LLM](https://telegra.ph/Arhitektura-VRAM-pochemu-padayut-lokalnye-LLM-i-kak-rasschitat-pamyat-09-09):** Подробный инженерный лонгрид с формулами и кодом.
- ⚡ **[DeepSeek R1 локально на ПК: запуск 14B, 32B и 70B без OOM](https://telegra.ph/DeepSeek-R1-lokalno-kak-zapustit-14B-32B-i-70B-na-PK-bez-OOM-09-09):** Конфиги llama.cpp (-fa, --ctk q8_0) и vLLM (--kv-cache-dtype fp8).

---

## 📊 Таблица Сравнения Моделей и Расхода VRAM

| Модель | Параметры | Квантование | VRAM (Веса) | VRAM (KV-кэш 16K) | Мин. GPU | Скорость (RTX 4090) | Контекст |
|---|---|---|---|---|---|---|---|
| **DeepSeek R1 Distill** | 14B | Q4_K_M | 9.1 GB | ~1.8 GB | RTX 3060 12GB | 28.5 tok/s | 64K |
| **Qwen 3.8 / 2.5 Coder** | 32B | Q4_K_M | 19.8 GB | ~3.8 GB (FP8) | RTX 4090 24GB | 42.0 tok/s | 64K |
| **DeepSeek R1 Distill** | 32B | Q4_K_M | 19.8 GB | ~4.2 GB (FP8) | RTX 4090 24GB | 38.0 tok/s | 64K |
| **Llama 3.3** | 70B | Q4_K_M | 43.0 GB | ~6.5 GB | 2x RTX 3090 / 4090 | 22.0 tok/s | 128K |
| **GLM-5.2** | 744B (MoE) | Q4_K_M | 24 GB + 64GB RAM | ~4.2 GB | RTX 4090 + RAM | 4.2 tok/s | 128K |
| **DeepSeek R1 Full** | 671B (MLA) | Q2_K + RAM | 24 GB + 128GB RAM| ~2.4 GB (MLA) | RTX 4090 + KTransformers | 14.0 tok/s | 128K |
| **Kimi K3** | 2.8T (MoE) | Q3_K_M | 48 GB + 128GB RAM| ~8.0 GB | 2x A100 / RTX 6000 Ada | 2.2 tok/s | 256K |

---

## 🚀 Быстрый запуск в 1 команду (llama.cpp & Ollama)

```bash
# 1. Запуск DeepSeek R1 14B в Ollama
ollama run deepseek-r1:14b

# 2. Оптимизированный запуск 32B в llama.cpp с FP8 KV-кэшем
./llama-server -m DeepSeek-R1-Distill-Qwen-32B-Q4_K_M.gguf -ngl 99 -c 16384 -fa --ctk q8_0 --ctv q8_0 --port 8080
```

---

## 🔗 Сообщество и Разработчики

- 📲 **Telegram-канал**: [@llm_hubs](https://t.me/llm_hubs) — ежедневная аналитика, шпаргалки и сорцы.
- 🌐 **Web Калькулятор**: [https://dangerousanen.github.io/llm-vram-calculator/](https://dangerousanen.github.io/llm-vram-calculator/)
- 💬 **Контакты и реклама**: [@ANENikita](https://t.me/ANENikita)
