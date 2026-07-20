# Update Template Content with Docupilot

Updates template content in Docupilot.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/dashboard/api/v2/templates/{id}/`
- **Base URL:** `https://api.docupilot.app`
- **Official documentation:** [Update Template Content](https://help.docupilot.app/developers/templates-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `file` | body | `file` | no |
