# List Tags with Calculoid

## Endpoint

- **Method:** `GET`
- **Path:** `/tags/:limit/:search`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [List Tags](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | path | `number` | yes | Maximum number of tags to return. |
| `search` | path | `string` | yes | Tag search text. |
