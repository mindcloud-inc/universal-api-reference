# Generate Presentation Outlines V3 with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/presentation/outlines/generate`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Generate Presentation Outlines V3](https://docs.presenton.ai/api-reference/v3-presentation/generate-outlines-sync-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | Prompt or source content for the outline. |
| `n_slides` | body | `number` | no | Number of slides to outline. |
| `include_title_slide` | body | `boolean` | no | Whether to include a title slide. |
