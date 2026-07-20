# Update Import Schema with Dromo

Updates an existing import schema in Dromo.

## Endpoint

- **Method:** `PUT`
- **Path:** `/schemas/:id/`
- **Base URL:** `https://app.dromo.io/api/v1`
- **Official documentation:** [Update Import Schema](https://developer.dromo.io/api-reference/import-schemas/update-an-import-schema)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
| `name` | body | `string` | yes | Request body field name. |
| `fields[]` | body | `array<object>` | yes | Request body field fields. |
| `settings` | body | `object` | yes | Request body field settings. |
| `hooks` | body | `object` | no | Request body field hooks. |
