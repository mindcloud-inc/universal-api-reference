# Search Collections with Dash.app

Finds collections in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/collection-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Collections](https://api-docs.dash.app/dash/openapi/collections/postcollectionsearch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `number` | yes | The item number to begin the result set from. |
| `pageSize` | body | `number` | yes | The maximum number of items to return. |
| `criterion` | body | `object` | yes | Dash collection search criterion object. |
| `sorts[]` | body | `array<object>` | no | Dash collection sort array. |
