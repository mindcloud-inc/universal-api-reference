# Create Presentation From JSON Async with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/create/from-json/async`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Create Presentation From JSON Async](https://docs.presenton.ai/api-reference/presentation/create-presentation-from-json-async-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Presentation title. |
| `template` | body | `string` | no | Template ID such as general. |
| `slides[]` | body | `array<object>` | yes | Slides array matching the template layouts. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
