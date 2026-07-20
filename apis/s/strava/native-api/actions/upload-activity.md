# Upload Activity with Strava

Creates a new activity upload in Strava.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploads`
- **Base URL:** `https://www.strava.com/api/v3`
- **Official documentation:** [Upload Activity](https://developers.strava.com/docs/reference/#api-Uploads-createUpload)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The activity file content or file reference. |
| `data_type` | body | `string` | yes | The uploaded file format such as fit, tcx, or gpx. |
| `name` | body | `string` | no | Optional activity name. |
| `description` | body | `string` | no | Optional activity description. |
| `external_id` | body | `string` | no | An external identifier for de-duplication. |
