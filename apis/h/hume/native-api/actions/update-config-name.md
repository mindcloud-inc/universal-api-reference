# Update config name with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/configs/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update config name](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI config identifier. |
| `name` | body | `string` | yes | New config name. |
