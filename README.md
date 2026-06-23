# telegram-offline-voice — Offline Telegram voice messages via Edge-TTS

> Generate natural-sounding Telegram voice messages locally using Microsoft Edge-TTS — zero token cost, 100% offline, with automatic Markdown cleaning and smart text segmentation.

[![OpenClaw Skill](https://img.shields.io/badge/OpenClaw-Skill-blueviolet)](https://github.com/NachaFromMars)

## Overview
telegram-offline-voice converts text to Telegram voice messages (OGG/Opus) using Microsoft Edge-TTS locally. It auto-strips Markdown symbols (`**bold**`, `#headers`, `[links]`) before synthesis so the audio sounds natural. Long text is split at sentence-ending punctuation into multiple voice bubbles for a more conversational feel. UUID-named temp files ensure safe concurrent use across multiple agents. Entirely offline after install — no API tokens consumed.

## Features
- **100% offline** — Edge-TTS, no cloud API cost
- **Markdown cleaner** — auto-removes `**`, `#`, `[link](url)` before TTS
- **Smart segmentation** — splits at `.!?` → multiple voice bubbles
- **UUID temp files** — safe concurrent multi-agent use
- **MP3 → OGG** — ffmpeg conversion for Telegram voice format
- **Script** — `voice_gen.py`

## Usage / Quick Start
```bash
# Install dependencies
apt install ffmpeg
uv pip install edge-tts
```
Then run `voice_gen.py` with your text.

## Trigger Keywords (OpenClaw)
voice message, telegram voice, offline TTS, generate voice, send voice message, 语音消息

## Related Skills
- [edge-tts](https://github.com/NachaFromMars/edge-tts) — Edge-TTS for non-Telegram use
- [tg-voice-whisper](https://github.com/NachaFromMars/tg-voice-whisper) — transcribe incoming voice messages

---
Part of the [NachaFromMars](https://github.com/NachaFromMars) OpenClaw skill ecosystem.
