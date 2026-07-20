# Execute SQL query with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/sql`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Execute SQL query](https://xata.io/docs/api-reference/gateway/execute-sql-query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | SQL query to execute (single query mode). |
| `params[]` | body | `array` | no | Positional parameters for the query (`$1`, `$2`, ...). |
| `queries[]` | body | `array` | no | Array of queries for batch execution within a single transaction. |
| `arrayMode` | body | `boolean` | no | Override array mode for this query (single query mode only). |
