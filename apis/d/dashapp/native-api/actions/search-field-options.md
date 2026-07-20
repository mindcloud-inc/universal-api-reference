# Search Field Options with Dash.app

Finds field options in Dash.app by search criteria.

## Endpoint

- **Method:** `POST`
- **Path:** `/field-option-searches`
- **Base URL:** `https://api-v2.dash.app`
- **Official documentation:** [Search Field Options](https://api-docs.dash.app/dash/openapi/field-options/postfieldoptionsearch)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `criterion` | body | `object` | yes |
| `from` | body | `number` | yes |
| `pageSize` | body | `number` | yes |
| `sorts[]` | body | `array<object>` | yes |
