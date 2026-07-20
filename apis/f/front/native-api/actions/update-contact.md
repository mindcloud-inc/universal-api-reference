# Update Contact with Front

Updates an existing contact in Front.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/:contact_id`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Update Contact](https://dev.frontapp.com/reference/update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | The contact ID. |
| `name` | body | `string` | no | Contact name. |
| `description` | body | `string` | no | Contact description. |
| `links[]` | body | `array<string>` | no | List of contact links. |
| `group_names[]` | body | `array<string>` | no | Deprecated list of group names. |
| `list_names[]` | body | `array<string>` | no | List of contact list names. |
| `custom_fields` | body | `object` | no | Contact custom fields object. |
