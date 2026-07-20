# Export Presentation V3 with Presenton

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/presentation/export`
- **Base URL:** `https://api.presenton.ai`
- **Official documentation:** [Export Presentation V3](https://docs.presenton.ai/api-reference/v3-presentation/export-presentation-as-pptx-or-pdf-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The presentation ID to export. |
| `export_as` | body | `string` | yes | Export format such as pptx or pdf. |
