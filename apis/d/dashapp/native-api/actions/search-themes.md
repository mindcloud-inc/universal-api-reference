# Search Themes with Dash.app

Finds themes in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/theme-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Themes](https://api-docs.dash.app/dash/openapi/theme/postthemesearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criterion` | body | `string` | yes | JSON string for the theme search criterion object. MindCloud currently serializes this Dash criterion correctly when provided as JSON text. |
| `from` | body | `number` | yes | Zero-based result offset. |
| `pageSize` | body | `number` | yes | Maximum number of results to return. |
| `sorts[]` | body | `array<object>` | yes | Array of theme sort objects. |
