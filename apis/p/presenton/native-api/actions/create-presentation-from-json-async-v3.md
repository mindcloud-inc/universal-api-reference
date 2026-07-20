# Create Presentation From JSON Async V3 with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/presentation/from-json/async`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Create Presentation From JSON Async V3](https://docs.presenton.ai/api-reference/v3-presentation/create-presentation-from-json-async-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | no | Presentation title. |
| `standard_template` | body | `string` | no | Standard template ID such as general. |
| `slides[]` | body | `array<object>` | yes | Slides array matching the template layouts. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
