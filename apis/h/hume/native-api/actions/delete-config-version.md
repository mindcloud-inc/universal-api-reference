# Delete config version with Hume

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0/evi/configs/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Delete config version](https://dev.hume.ai/reference/speech-to-speech-evi/configs/delete-config-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI config identifier. |
| `version` | path | `number` | yes | Version number. |
