# Create Prompt with Hume AI

Creates a new EVI prompt in Hume AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/prompts`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create Prompt](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Prompt name. |
| `text` | body | `string` | yes | Prompt text. |
