# Export Presentation with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/ppt/presentation/export`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Export Presentation](https://docs.presenton.ai/api-reference/presentation/export-presentation-as-pptx-or-pdf-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The presentation ID to export. |
| `export_as` | body | `string` | no | Export format such as pptx or pdf. |
