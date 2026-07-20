# Create Speech with Groq

Creates speech from text in Groq.

## Endpoint

- **Method:** `POST`
- **Path:** `/openai/v1/audio/speech`
- **Base URL:** `https://api.groq.com`
- **Official documentation:** [Create Speech](https://console.groq.com/docs/api-reference#audio-speech)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `model` | body | `string` | yes |
| `input` | body | `string` | yes |
| `voice` | body | `string` | yes |
| `response_format` | body | `list` | no |
| `sample_rate` | body | `list` | no |
| `speed` | body | `number` | no |
