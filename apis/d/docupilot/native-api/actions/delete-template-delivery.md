# Delete Template Delivery with Docupilot

Deletes a template delivery from Docupilot.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/dashboard/api/v2/templates/{template_id}/deliveries/{id}/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Delete Template Delivery](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `template_id` | path | `number` | yes |
