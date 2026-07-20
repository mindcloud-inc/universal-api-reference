# List Generated Documents with Docupilot

Retrieves generated document history from Docupilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboard/api/v2/history/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [List Generated Documents](https://help.docupilot.app/developers/templates-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ordering` | query | `string` | no | Which field to use when ordering the results. |
| `page` | query | `number` | no | A page number within the paginated result set. |
