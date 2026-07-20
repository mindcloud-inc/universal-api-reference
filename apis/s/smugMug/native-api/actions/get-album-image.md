# Get Album Image with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/album/:albumKey/image/:imageUriId`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [Get Album Image](https://api.smugmug.com/api/v2/doc/reference/album-image.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `albumKey` | path | `string` | yes | SmugMug album key. |
| `imageUriId` | path | `string` | yes | SmugMug image identifier including any URI suffix. |
