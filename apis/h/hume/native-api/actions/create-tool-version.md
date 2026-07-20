# Create tool version with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/tools/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create tool version](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI tool identifier. |
| `parameters` | body | `string` | yes | Stringified JSON Schema defining tool parameters. |
| `description` | body | `string` | no | Optional tool description. |
| `fallback_content` | body | `string` | no | Optional fallback response content. |
| `version_description` | body | `string` | no | Optional tool version description. |
