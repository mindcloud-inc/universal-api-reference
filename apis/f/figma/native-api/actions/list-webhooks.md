# List Webhooks with Figma

Retrieves webhooks from Figma.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.figma.com/v2/webhooks`
- **Base URL:** `https://api.figma.com/v1`
- **Official documentation:** [List Webhooks](https://developers.figma.com/docs/rest-api/webhooks-endpoints/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `context` | query | `list` | no | Filter by context type: team, project, or file. |
| `context_id` | query | `string` | no | Context identifier to filter webhook results. |
| `plan_api_id` | query | `string` | no | Plan identifier to list webhooks across accessible contexts. |
| `cursor` | query | `string` | no | Pagination cursor when listing by plan_api_id. |
