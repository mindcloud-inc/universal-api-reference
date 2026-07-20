# Get Image Metadata with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/image/:imageUriId!metadata`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [Get Image Metadata](https://api.smugmug.com/api/v2/doc/reference/image.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUriId` | path | `string` | yes | SmugMug image identifier including any URI suffix. |
