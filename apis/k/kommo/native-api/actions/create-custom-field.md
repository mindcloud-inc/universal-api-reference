# Create Custom Field with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/:entity_type/custom_fields`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Custom Field](https://developers.kommo.com/reference/add-custom-fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | path | `string` | yes | Entity type. |
| `entity_type` | path | `string` | no | Required path parameter for Create Custom Field. |
| `name` | body | `string` | yes | Custom field name. |
| `type` | body | `string` | yes | Custom field type. |
| `code` | body | `string` | no | Custom field code. |
| `sort` | body | `number` | no | Custom field sort order. |
| `enums[]` | body | `array<object>` | no | Custom field enums payload. |
