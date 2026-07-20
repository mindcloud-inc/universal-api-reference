# Get Video File Download Url with VdoCipher

Retrieves a video file download URL from VdoCipher.

## Endpoint

- **Method:** `GET`
- **Path:** `/videos/:videoId/files/:fileId`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Get Video File Download Url](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `videoId` | path | `string` | yes |
| `fileId` | path | `string` | yes |
