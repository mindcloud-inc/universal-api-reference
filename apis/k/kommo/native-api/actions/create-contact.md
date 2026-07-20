# Create Contact with Kommo

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://{referer}/api/v4`
- **Official documentation:** [Create Contact](https://developers.kommo.com/reference/add-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Contact name. |
| `first_name` | body | `string` | no | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `responsible_user_id` | body | `number` | no | Responsible user ID. |
| `custom_fields_values[]` | body | `array<object>` | no | Custom field values payload. |
| `_embedded` | body | `object` | no | Embedded payload. |
| `tags_to_add[]` | body | `array<object>` | no | Tags to add payload. |
