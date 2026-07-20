# Run Query with Logfire

Runs a query against Logfire data.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/query`
- **Base URL:** `https://logfire-api.pydantic.dev`
- **Official documentation:** [Run Query](https://pydantic.dev/docs/logfire/manage/query-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sql` | query | `string` | yes | SQL query to execute against the Logfire project. |
| `limit` | query | `number` | no | Maximum number of rows to return. Logfire defaults to 500 and allows up to 10,000. |
| `min_timestamp` | query | `date` | no | Lower timestamp bound for records or metrics returned by the query. |
| `max_timestamp` | query | `date` | no | Upper timestamp bound for records or metrics returned by the query. |
