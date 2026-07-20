# Convert text to speech with 1minAI

Creates speech audio from text in 1minAI.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/features`
- **Base URL:** `https://api.1min.ai`
- **Official documentation:** [Convert text to speech](https://docs.1min.ai/docs/api/ai-for-audio/text-to-speech/openai)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `text` | body | `string` | yes | — |
| `voice` | body | `list` | no | Accepted values: `Alloy`, `Echo`, `Fable`, `Nova`, `Onyx`, `Shimmer`. |
| `responseFormat` | body | `list` | no | Accepted values: `AAC`, `FLAC`, `MP3`, `Opus`, `PCM`, `WAV`. |
| `speed` | body | `number` | no | — |
