# Update Folder with Docupilot

Updates an existing folder in Docupilot.

## Endpoint

- **Method:** `PUT`
- **Path:** `/dashboard/api/v2/folders/{id}/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Update Folder](https://help.docupilot.app/developers/folders-api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `name` | body | `string` | yes |
