# Create Saved Search with Dash.app

Creates a new saved search in Dash.app.

## Endpoint

- **Method:** `POST`
- **Path:** `/saved-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Create Saved Search](https://api-docs.dash.app/dash/openapi/saved-searches/postsavedsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `criterion` | body | `object` | yes | Dash criterion object |
| `emailUserOnNewUploads` | body | `boolean` | yes | Whether to email the user when new uploads match |
| `name` | body | `string` | yes | Saved search name |
| `sorts[]` | body | `array<object>` | yes | Dash sorts array |
