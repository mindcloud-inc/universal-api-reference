# Get File Download URL with Needle

Retrieves a signed file download URL from Needle.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/files/:fileId/download_url`
- **Base URL:** `https://needle.app`
- **Official documentation:** [Get File Download URL](https://docs.needle.app/docs/api-reference/get-download-url/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | ID of the file to generate a download URL for |
