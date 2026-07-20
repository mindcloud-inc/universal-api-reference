# Update Video Chapters with VdoCipher

Updates video chapters in VdoCipher.

## Endpoint

- **Method:** `PUT`
- **Path:** `/videos/:videoId/chapters`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Update Video Chapters](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `chapters` | body | `string` | no |
| `videoId` | path | `string` | no |
