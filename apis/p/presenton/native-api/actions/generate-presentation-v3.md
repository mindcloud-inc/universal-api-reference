# Generate Presentation V3 with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/presentation/generate`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Generate Presentation V3](https://docs.presenton.ai/api-reference/v3-presentation/generate-presentation-sync-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Prompt or source content for the presentation. |
| `n_slides` | body | `number` | no | Number of slides to generate. |
| `standard_template` | body | `string` | no | Standard template ID such as general. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
