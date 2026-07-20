# List Folder Albums with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/folder/user/:nickname!albums`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [List Folder Albums](https://api.smugmug.com/api/v2/doc/reference/folder.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nickname` | path | `string` | yes | SmugMug account nickname. |
