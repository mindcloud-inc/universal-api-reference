# Generate Presentation with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/generate`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Generate Presentation](https://docs.presenton.ai/api-reference/presentation/generate-presentation-sync-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Prompt or source content for the presentation. |
| `n_slides` | body | `number` | no | Number of slides to generate. |
| `template` | body | `string` | no | Template ID such as general. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
