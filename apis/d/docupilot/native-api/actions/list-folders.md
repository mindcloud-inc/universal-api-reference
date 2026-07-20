# List Folders with Docupilot

Retrieves folders from Docupilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/dashboard/api/v2/folders/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [List Folders](https://help.docupilot.app/developers/folders-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ordering` | query | `string` | no | Which field to use when ordering the results. |
| `permission` | query | `list` | no | Accepted values: `manage`, `read`, `write`. |
