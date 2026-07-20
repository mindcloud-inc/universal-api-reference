# Update Company with Kommo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Update Company](https://developers.kommo.com/reference/updating-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Company ID. |
| `name` | body | `string` | no | Company name. |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `custom_fields_values[]` | body | `array<object>` | no | Custom field values payload. |
| `_embedded` | body | `object` | no | Embedded payload. |
| `request_id` | body | `string` | no | Request identifier. |
| `tags_to_add[]` | body | `array<object>` | no | Tags to add payload. |
| `tags_to_delete[]` | body | `array<object>` | no | Tags to delete payload. |
