# List Album Images with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/album/:albumKey!images`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [List Album Images](https://api.smugmug.com/api/v2/doc/reference/album.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `albumKey` | path | `string` | yes | SmugMug album key. |
