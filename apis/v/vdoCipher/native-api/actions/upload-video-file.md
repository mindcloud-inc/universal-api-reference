# Upload Video File with VdoCipher

Uploads a poster or subtitle file to VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId/files`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Upload Video File](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `file` | body | `string` | no |
| `videoId` | path | `string` | no |
