# Get prompt version with Hume

## Endpoint

- **Method:** `GET`
- **Path:** `/v0/evi/prompts/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Get prompt version](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/get-prompt-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI prompt identifier. |
| `version` | path | `number` | yes | Version number. |
