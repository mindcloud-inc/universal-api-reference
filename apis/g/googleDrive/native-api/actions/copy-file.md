# Copy File with Google Drive

Creates a copy of a file in Google Drive.

## Endpoint

- **Method:** `POST`
- **Path:** `/drive/v3/files/:fileId/copy`
- **Base URL:** `https://www.googleapis.com`
- **Official documentation:** [Copy File](https://developers.google.com/workspace/drive/api/reference/rest/v3/files/copy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `fileId` | path | `string` | no |
| `mimeType` | body | `string` | no |
