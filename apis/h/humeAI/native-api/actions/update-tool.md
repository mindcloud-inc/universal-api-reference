# Update Tool with Hume AI

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v0/evi/tools/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Update Tool](https://dev.hume.ai/reference/speech-to-speech-evi/tools/update-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Tool ID. |
| `name` | body | `string` | yes | Updated tool name. |
