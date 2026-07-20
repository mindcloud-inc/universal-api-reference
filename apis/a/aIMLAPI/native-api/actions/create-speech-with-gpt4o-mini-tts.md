# Create Speech With GPT-4o Mini TTS with AI/ML API

Creates speech with GPT-4o Mini TTS in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tts`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create Speech With GPT-4o Mini TTS](https://docs.aimlapi.com/api-references/speech-models/text-to-speech/openai/gpt-4o-mini-tts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `response_format` | body | `string` | no |
| `speed` | body | `number` | no |
| `style` | body | `string` | no |
| `text` | body | `string` | yes |
| `voice` | body | `string` | no |
