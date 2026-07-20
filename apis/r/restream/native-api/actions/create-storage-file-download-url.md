# Create Storage File Download URL with Restream

Generates a download URL for a storage file in Restream.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/storage/files/:fileId/download-url`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Create Storage File Download URL](https://developers.restream.io/storage/storage-file-download-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The ID of the storage file whose download URL to generate. |
