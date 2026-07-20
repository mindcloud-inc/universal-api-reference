# Update tool name with Hume

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/tools/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update tool name](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool-name)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI tool identifier. |
| `name` | body | `string` | yes | New tool name. |
