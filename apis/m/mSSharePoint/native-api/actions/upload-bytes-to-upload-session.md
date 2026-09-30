# Upload Bytes to Upload Session with MS SharePoint

## Endpoint

- **Method:** `PUT`
- **URL:** `:uploadUrl`
- **Official documentation:** [Upload Bytes to Upload Session](https://learn.microsoft.com/en-us/graph/api/driveitem-createuploadsession?view=graph-rest-1.0#example-2-upload-bytes-to-the-upload-session)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uploadUrl` | path | `string` | yes | The full uploadUrl returned by Create Upload Session. |
| `file` | body | `file` | yes | The file or file fragment to upload in this request. |
| `Content-Range` | path | `string` | yes | The byte range and total file size, such as bytes 0-327679/655360. |
