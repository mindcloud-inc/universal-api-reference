# Create Template Delivery with Docupilot

Creates a template delivery in Docupilot.

## Endpoint

- **Method:** `POST`
- **Path:** `/dashboard/api/v2/templates/{template_id}/deliveries/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Create Template Delivery](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `number` | yes | — |
| `payload` | body | `object` | no | Provide a JSON object that matches the documented Docupilot request body. |
