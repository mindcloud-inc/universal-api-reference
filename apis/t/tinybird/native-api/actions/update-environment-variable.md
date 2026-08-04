# Update Environment Variable with Tinybird

## Endpoint

- **Method:** `PUT`
- **Path:** `v0/variables/:name`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Update Environment Variable](https://www.tinybird.co/docs/api-reference/environment-variables-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | path | `string` | yes | The environment variable name. |
| `value` | body | `string` | yes | The new value to store. |
