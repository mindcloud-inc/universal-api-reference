# Derive Presentation with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/derive`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Derive Presentation](https://docs.presenton.ai/api-reference/presentation/derive-presentation-from-existing-one)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | body | `string` | yes | The source presentation ID. |
| `slides[]` | body | `array<object>` | yes | Slides array with updates for the derived deck. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
