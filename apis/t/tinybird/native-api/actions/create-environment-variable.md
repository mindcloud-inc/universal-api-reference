# Create Environment Variable with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/variables`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Create Environment Variable](https://www.tinybird.co/docs/api-reference/environment-variables-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The environment variable name. |
| `type` | body | `string` | no | Optional variable type; Tinybird defaults to secret. |
| `value` | body | `string` | yes | The value to store. |
