# Create Upload Link with pixx.io

Creates a new upload link in your pixx.io workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadLinks`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Create Upload Link](https://api.pixxio.com/docs/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | The upload link description. |
| `directoryID` | body | `number` | no | The directory the upload link points to. |
| `name` | body | `string` | yes | The upload link name. |
| `validityPeriod` | body | `string` | no | How long the upload link remains valid. |
