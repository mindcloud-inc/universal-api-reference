# Create tool with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/tools`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create tool](https://dev.hume.ai/reference/speech-to-speech-evi/tools/create-tool)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tool name. |
| `parameters` | body | `string` | yes | Stringified JSON Schema defining tool parameters. |
| `description` | body | `string` | no | Optional tool description. |
| `fallback_content` | body | `string` | no | Optional fallback response content. |
| `version_description` | body | `string` | no | Optional tool version description. |
