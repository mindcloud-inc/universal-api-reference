# Run SQL Query with Data Blaze

Runs a SQL query in Data Blaze.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/database/1OzRoKyYgXpIR32FUO1JMm/query/`
- **Base URL:** `https://data-api.blaze.today`
- **Official documentation:** [Run SQL Query](https://blaze.today/datablaze/docs/apis/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | BSQL query to run inside the Data Blaze space. |
