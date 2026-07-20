# Update Custom Field with Kommo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:entity_type/custom_fields/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Update Custom Field](https://developers.kommo.com/reference/update-custom-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Entity type. |
| `entity_type` | path | `string` | no | Required path parameter for Update Custom Field. |
| `id` | path | `number` | yes | Custom field ID. |
| `name` | body | `string` | no | Custom field name. |
| `type` | body | `string` | no | Custom field type. |
| `code` | body | `string` | no | Custom field code. |
| `sort` | body | `number` | no | Custom field sort order. |
| `enums[]` | body | `array<object>` | no | Custom field enums payload. |
