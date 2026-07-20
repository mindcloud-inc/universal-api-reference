# Update prompt name with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/prompts/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update prompt name](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI prompt identifier. |
| `name` | body | `string` | yes | New prompt name. |
