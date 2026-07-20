# Create Direct Link with pixx.io

Creates a new direct link in your pixx.io workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/directLinks`
- **Base URL:** `https://mindcloudpixx260413.px.media/api/v1`
- **Official documentation:** [Create Direct Link](https://api.pixxio.com/docs/openapi)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `downloadType` | body | `string` | no | Download type such as original, preview, custom, or downloadFormat. |
| `fileExtension` | body | `string` | no | Output file extension when using custom conversion settings. |
| `fileID` | body | `number` | yes | The file ID for the direct link. |
| `fileName` | body | `string` | yes | The direct link file name without file extension. |
