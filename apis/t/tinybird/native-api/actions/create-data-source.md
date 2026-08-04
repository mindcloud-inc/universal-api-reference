# Create Data Source with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/datasources`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Create Data Source](https://www.tinybird.co/docs/api-reference/datasource-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Data source name |
| `schema` | body | `string` | yes | Tinybird schema, for example: event_id UInt64, created_at DateTime |
