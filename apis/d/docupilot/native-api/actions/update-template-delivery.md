# Update Template Delivery with Docupilot

Updates an existing template delivery in Docupilot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dashboard/api/v2/templates/{template_id}/deliveries/{id}/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Update Template Delivery](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `template_id` | path | `number` | yes | — |
| `payload` | body | `object` | no | Provide a JSON object that matches the documented Docupilot request body. |
