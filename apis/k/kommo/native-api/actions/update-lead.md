# Update Lead with Kommo

## Endpoint

- **Method:** `PATCH`
- **Path:** `/leads/:id`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Update Lead](https://developers.kommo.com/reference/updating-single-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Lead ID. |
| `name` | body | `string` | no | Lead name. |
| `price` | body | `number` | no | Lead price. |
| `status_id` | body | `number` | no | Lead status ID. |
| `pipeline_id` | body | `number` | no | Lead pipeline ID. |
| `loss_reason_id` | body | `number` | no | Loss reason ID. |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `custom_fields_values[]` | body | `array<object>` | no | Custom field values payload. |
| `_embedded` | body | `object` | no | Embedded payload. |
| `request_id` | body | `string` | no | Request identifier. |
| `tags_to_add[]` | body | `array<object>` | no | Tags to add payload. |
| `tags_to_delete[]` | body | `array<object>` | no | Tags to delete payload. |
