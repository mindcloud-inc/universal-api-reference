# Alter Data Source with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/datasources/:name/alter`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Alter Data Source](https://www.tinybird.co/docs/api-reference/datasource-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional data source description |
| `dry` | body | `boolean` | no | When true, validate without modifying the data source |
| `name` | path | `string` | yes | The data source name to target. |
| `schema` | body | `string` | no | Schema additions or replacements to apply |
