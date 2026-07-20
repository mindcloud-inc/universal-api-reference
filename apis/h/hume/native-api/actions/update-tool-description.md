# Update tool description with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/tools/:id/version/:version`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update tool description](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool-description)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI tool identifier. |
| `version` | path | `number` | yes | Version number. |
| `version_description` | body | `string` | yes | Updated tool version description. |
