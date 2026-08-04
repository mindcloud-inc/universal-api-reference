# Delete Matching Data with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/datasources/:name/delete`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Delete Matching Data](https://www.tinybird.co/docs/api-reference/datasource-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `delete_condition` | body | `string` | yes | Required SQL WHERE condition; no DELETE keyword |
| `dry_run` | body | `boolean` | no | When true, validate and report matching rows without deleting |
| `name` | path | `string` | yes | The data source name to target. |
