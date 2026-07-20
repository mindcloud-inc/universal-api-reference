# Edit Presentation with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/edit`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Edit Presentation](https://docs.presenton.ai/api-reference/presentation/edit-presentation-with-new-content)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `presentation_id` | body | `string` | yes | The presentation ID to edit. |
| `slides[]` | body | `array<object>` | yes | Slides array with updates to apply. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
