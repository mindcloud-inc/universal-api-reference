# Query Marketing Data with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/data_query`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Query Marketing Data](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Supermetrics data source ID to query. |
| `ds_accounts[]` | body | `array<string>` | no | Account IDs from Discover Accounts. |
| `fields[]` | body | `array<string>` | no | Metric and dimension field IDs to query. |
| `date_range_type` | body | `string` | no | Use custom with start and end dates, or a documented relative range such as last_7_days. |
| `start_date` | body | `date` | no | Start date in YYYY-MM-DD format when date range type is custom. |
| `end_date` | body | `date` | no | End date in YYYY-MM-DD format when date range type is custom. |
| `timezone` | body | `string` | no | Optional IANA timezone for date calculations. |
| `filters` | body | `string` | no | Optional Supermetrics filter expression. |
| `max_rows` | body | `number` | no | Maximum rows to return. |
