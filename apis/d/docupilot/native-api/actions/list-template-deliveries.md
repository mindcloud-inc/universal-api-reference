# List Template Deliveries with Docupilot

Retrieves template deliveries from Docupilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboard/api/v2/templates/{template_id}/deliveries/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [List Template Deliveries](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `number` | yes | — |
| `ordering` | query | `string` | no | Which field to use when ordering the results. |
