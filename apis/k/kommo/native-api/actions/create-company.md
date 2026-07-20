# Create Company with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/companies`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Company](https://developers.kommo.com/reference/add-companies)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Company name. |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `custom_fields_values[]` | body | `array<object>` | no | Custom field values payload. |
| `_embedded` | body | `object` | no | Embedded payload. |
| `request_id` | body | `string` | no | Request identifier. |
| `tags_to_add[]` | body | `array<object>` | no | Tags to add payload. |
