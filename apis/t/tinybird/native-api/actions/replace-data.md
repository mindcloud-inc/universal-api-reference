# Replace Data with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/datasources`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Replace Data](https://www.tinybird.co/docs/api-reference/datasource-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | no | Optional source format: csv, ndjson, or parquet |
| `name` | body | `string` | yes | Target data source name |
| `url` | body | `string` | yes | Remote file URL to use as replacement data |
