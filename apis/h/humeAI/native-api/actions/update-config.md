# Update Config with Hume AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/configs/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update Config](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Config ID. |
| `name` | body | `string` | yes | Updated config name. |
