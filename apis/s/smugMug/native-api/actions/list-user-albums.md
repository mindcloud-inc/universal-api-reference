# List User Albums with SmugMug

## Endpoint

- **Method:** `GET`
- **Path:** `/user/:nickname!albums`
- **Base URL:** `https://api.smugmug.com/api/v2`
- **Official documentation:** [List User Albums](https://api.smugmug.com/api/v2/doc/reference/user.html)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nickname` | path | `string` | yes | SmugMug account nickname. |
