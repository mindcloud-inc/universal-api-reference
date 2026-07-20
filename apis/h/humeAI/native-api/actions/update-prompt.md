# Update Prompt with Hume AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/prompts/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update Prompt](https://dev.hume.ai/reference/speech-to-speech-evi/prompts/update-prompt)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Prompt ID. |
| `name` | body | `string` | yes | Updated prompt name. |
