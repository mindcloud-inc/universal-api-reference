# Get Async Query Results with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/get_async_query_results`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Get Async Query Results](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `schedule_id` | body | `string` | yes | Opaque schedule_id returned by Query Marketing Data. |
| `compress` | body | `boolean` | no | Return a compact TOON response instead of JSON when supported. |
