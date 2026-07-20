# Convert Asset to Base64 with 1001fx

Converts an asset or URL into a base64 string.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/asset2base64`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Convert Asset to Base64](https://1001fx.com/functions/asset2base64)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `addPrefix` | body | `boolean` | no |
| `file` | body | `file` | no |
| `url` | body | `string` | no |
