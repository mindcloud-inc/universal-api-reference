# Create Import Schema with Dromo

Creates a new import schema in Dromo.

## Endpoint

- **Method:** `POST`
- **Path:** `/schemas/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Create Import Schema](https://developer.dromo.io/api-reference/import-schemas/create-a-new-import-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Request body field name. |
| `fields[]` | body | `array<object>` | yes | Request body field fields. |
| `settings` | body | `object` | yes | Request body field settings. |
| `hooks` | body | `object` | no | Request body field hooks. |
