# Create prompt with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/prompts`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create prompt](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Prompt name. |
| `text` | body | `string` | yes | Prompt instructions text. |
| `version_description` | body | `string` | no | Optional prompt version description. |
