# Generate Presentation Async with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/generate/async`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Generate Presentation Async](https://docs.presenton.ai/api-reference/presentation/generate-presentation-async-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Prompt or source content for the presentation. |
| `n_slides` | body | `number` | no | Number of slides to generate. |
| `template` | body | `string` | no | Template ID such as general. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
