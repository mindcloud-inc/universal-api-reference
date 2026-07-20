# Discover Fields with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/field_discovery`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Discover Fields](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Supermetrics data source ID to inspect fields for. |
| `filter` | body | `string` | no | Optional field filter string. |
| `compress` | body | `boolean` | no | Return a compact TOON response instead of JSON when supported. |
