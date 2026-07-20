# Search Saved Searches with Dash.app

Finds saved searches in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/saved-search-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Saved Searches](https://api-docs.dash.app/dash/openapi/saved-searches/postsavedsearchsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criterion` | body | `object` | yes | Saved search criterion object. |
| `from` | body | `number` | yes | Zero-based result offset. |
| `pageSize` | body | `number` | yes | Maximum number of results to return. |
| `sorts[]` | body | `array<object>` | yes | Array of saved search sort objects. |
