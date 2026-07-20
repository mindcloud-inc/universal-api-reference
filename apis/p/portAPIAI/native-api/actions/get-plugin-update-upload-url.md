# Get Plugin Update Upload URL with Port API AI

Retrieves a plugin update upload URL from Port.

## Endpoint

- **Method:** `PUT`
- **Path:** `/plugins/:identifier/upload-url`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Plugin Update Upload URL](https://docs.port.io/api-reference/get-a-presigned-url-for-plugin-updates)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | The Port plugin identifier. |
