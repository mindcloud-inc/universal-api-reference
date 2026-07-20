# Create Speech With TTS-1 HD with AI/ML API

Creates speech with TTS-1 HD in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tts`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create Speech With TTS-1 HD](https://docs.aimlapi.com/api-references/speech-models/text-to-speech/openai/tts-1-hd)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `response_format` | body | `string` | no |
| `speed` | body | `number` | no |
| `style` | body | `string` | no |
| `text` | body | `string` | yes |
| `voice` | body | `string` | no |
