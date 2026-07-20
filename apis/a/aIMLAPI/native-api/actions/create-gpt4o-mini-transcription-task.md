# Create GPT-4o Mini Transcription Task with AI/ML API

Creates a GPT-4o Mini transcription task in AI/ML API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/stt/create`
- **Base URL:** `https://api.aimlapi.com`
- **Official documentation:** [Create GPT-4o Mini Transcription Task](https://docs.aimlapi.com/api-references/speech-models/speech-to-text/openai/gpt-4o-mini-transcribe)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `language` | body | `string` | no |
| `prompt` | body | `string` | no |
| `temperature` | body | `number` | no |
| `url` | body | `string` | yes |
