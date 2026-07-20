# Create Contact with Front

Creates a new contact in Front.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [Create Contact](https://dev.frontapp.com/reference/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `avatar` | body | `file` | no | — |
| `links[]` | body | `array<string>` | no | — |
| `group_names[]` | body | `array<string>` | no | Deprecated by Front. Prefer `list_names`. |
| `list_names[]` | body | `array<string>` | no | — |
| `custom_fields` | body | `object` | no | — |
| `handles[]` | body | `array<object>` | yes | JSON array of Front handle objects, for example [{"handle":"person@example.com","source":"email"}]. |
