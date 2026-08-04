# Update Static Token with Tinybird

## Endpoint

- **Method:** `PUT`
- **Path:** `v0/tokens/:token`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Update Static Token](https://www.tinybird.co/docs/api-reference/token-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional Markdown description. |
| `name` | body | `string` | no | Optional new static token name. |
| `scope` | body | `string` | no | Optional replacement scope. |
| `token` | path | `string` | yes | The static token name. |
