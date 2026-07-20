# Delete tool version with Hume

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v0/evi/tools/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Delete tool version](https://dev.hume.ai/reference/speech-to-speech-evi/tools/delete-tool-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI tool identifier. |
| `version` | path | `number` | yes | Version number. |
