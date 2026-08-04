# Create Static Token with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/tokens`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Create Static Token](https://www.tinybird.co/docs/api-reference/token-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The static token name. |
| `scope` | body | `string` | yes | A Tinybird static-token scope. |
