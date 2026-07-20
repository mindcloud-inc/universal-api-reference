# Delete prompt version with Hume

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0/evi/prompts/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Delete prompt version](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/delete-prompt-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI prompt identifier. |
| `version` | path | `number` | yes | Version number. |
