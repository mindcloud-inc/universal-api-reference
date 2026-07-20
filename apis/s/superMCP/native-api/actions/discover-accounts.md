# Discover Accounts with SuperMCP

## Endpoint

- **Method:** `POST`
- **Path:** `/mcp/accounts_discovery`
- **Base URL:** `https://mcp.supermetrics.com`
- **Official documentation:** [Discover Accounts](https://mcp.supermetrics.com/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ds_id` | body | `string` | yes | Supermetrics data source ID, such as GAWA for Google Analytics 4 or AW for Google Ads. |
| `filter` | body | `string` | no | Optional case-insensitive account filter against account ID, name, or group. |
| `compress` | body | `boolean` | no | Return a compact TOON response instead of JSON when supported. |
