# List Content Blocks with Docupilot

Retrieves content blocks from Docupilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboard/api/v2/content_blocks/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [List Content Blocks](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ordering` | query | `string` | no | Which field to use when ordering the results. |
| `page` | query | `number` | no | A page number within the paginated result set. |
| `search` | query | `string` | no | A search term. |
