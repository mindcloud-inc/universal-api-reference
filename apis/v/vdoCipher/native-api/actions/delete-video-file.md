# Delete Video File with VdoCipher

Deletes an existing video file from VdoCipher.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/videos/:videoId/files/:fileId`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Delete Video File](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `videoId` | path | `string` | yes |
| `fileId` | path | `string` | yes |
