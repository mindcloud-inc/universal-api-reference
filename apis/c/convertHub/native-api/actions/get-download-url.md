# Get Download URL with ConvertHub

Retrieves a converted file URL or base64 content from ConvertHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/jobs/:jobId/download`
- **Base URL:** `https://api.converthub.com/v2`
- **Official documentation:** [Get Download URL](https://converthub.com/api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | — |
| `format` | query | `list` | no | Set to base64 to return the file content as a base64-encoded string instead of a download URL. Accepted values: `base64`. |
