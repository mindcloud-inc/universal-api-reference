# Execute SQL Query with Tinybird

## Endpoint

- **Method:** `POST`
- **Path:** `v0/sql`
- **Base URL:** `{apiHost}`
- **Official documentation:** [Execute SQL Query](https://www.tinybird.co/docs/api-reference/sql-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | body | `string` | yes | The SQL query to execute. |
