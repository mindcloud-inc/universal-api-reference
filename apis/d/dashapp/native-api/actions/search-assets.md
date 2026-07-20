# Search Assets with Dash.app

Finds assets in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/asset-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Assets](https://api-docs.dash.app/dash/openapi/assets/postassetsearch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `action` | body | `string` | no |
| `criterion` | body | `object` | yes |
| `from` | body | `number` | yes |
| `pageSize` | body | `number` | yes |
| `sorts[]` | body | `array<object>` | yes |
