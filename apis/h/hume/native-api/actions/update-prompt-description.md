# Update prompt description with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/prompts/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update prompt description](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt-description)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI prompt identifier. |
| `version` | path | `number` | yes | Version number. |
| `version_description` | body | `string` | yes | Updated prompt version description. |
