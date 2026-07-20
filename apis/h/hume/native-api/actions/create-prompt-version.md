# Create prompt version with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/prompts/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create prompt version](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/create-prompt-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI prompt identifier. |
| `text` | body | `string` | yes | Prompt instructions text for the new version. |
| `version_description` | body | `string` | no | Optional prompt version description. |
