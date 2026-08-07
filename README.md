# Open-Source LLM Benchmarks & VRAM Requirements (2026) ⚡️

[![Telegram Channel](https://img.shields.io/badge/Telegram-@llm__hubs-2CA5E0?style=for-the-badge&logo=telegram)](https://t.me/llm_hubs)
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38/media/badge.svg)](https://github.com/DangerousANEN/awesome-llm-benchmarks-2026)

Сравнительная таблица производительности, скорости инференса (tok/s) и реального потребления VRAM/RAM открытых SOTA моделей 2026 года: **GLM-5.2, Kimi K3, DeepSeek V4, Qwen 2.5 Coder, Llama 3.3**.

> 📢 **Официальный Telegram-канал проекта:**  
> Все обновления моделей, новые навыки, бенчмарки и инструменты сжатия контекста публикуются в канале **[.LLMhub (@llm_hubs)](https://t.me/llm_hubs)**.

---

## 📊 Таблица Сравнения Моделей

| Модель | Параметры | Формат Квантования | VRAM (Мин.) | Скорость (RTX 4090 / 5090) | Контекст | Ссылка |
|---|---|---|---|---|---|---|
| **GLM-5.2** | 744B (MoE) | Q4_K_M | 24 GB + 64GB RAM | 4.2 tok/s | 128K | [HuggingFace](https://huggingface.co) |
| **DeepSeek V4 Pro** | 671B (MoE) | Q4_K_S | 24 GB + 48GB RAM | 6.5 tok/s | 128K | [GitHub](https://github.com/deepseek-ai) |
| **Qwen 2.5 Coder** | 32B | Q8_0 | 34 GB | 45.0 tok/s | 64K | [GitHub](https://github.com/QwenLM) |
| **Kimi K3** | 2.8T (MoE) | Q3_K_M | 48 GB + 128GB RAM | 2.2 tok/s | 256K | [HuggingFace](https://huggingface.co) |

---

## 🚀 Быстрый запуск в 1 команду (Ollama & Colibrì)

```bash
# Запуск Qwen 2.5 Coder локально
ollama run qwen2.5-coder:32b

# Запуск GLM-5.2 через Colibri C-Engine
./colibri serve --model glm-5.2-744b --vram-limit 24GB
```

---

## 🔗 Подписка и Сообщество

- 📲 **Telegram-канал**: [@llm_hubs](https://t.me/llm_hubs)
- 💬 **Обсуждение и саппорт**: [@mosaicsup](https://t.me/mosaicsup)
