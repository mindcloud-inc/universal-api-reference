# Update config description with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/configs/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update config description](https://dev.hume.ai/reference/speech-to-speech-evi/configs/update-config-description)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI config identifier. |
| `version` | path | `number` | yes | Version number. |
| `version_description` | body | `string` | yes | Updated config version description. |
