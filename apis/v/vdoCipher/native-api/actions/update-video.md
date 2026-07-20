# Update Video with VdoCipher

Updates an existing video in VdoCipher.

## Endpoint

- **Method:** `POST`
- **Path:** `/videos/:videoId`
- **Base URL:** `https://dev.vdocipher.com/api`
- **Official documentation:** [Update Video](https://www.vdocipher.com/docs/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `title` | body | `string` | no |
| `videoId` | path | `string` | no |
