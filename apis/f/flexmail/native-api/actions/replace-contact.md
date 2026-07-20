# Replace Contact with Flexmail

Replaces an existing contact in Flexmail.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/{id}`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Replace Contact](https://api.flexmail.eu/documentation/#put-/contacts/-id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `email` | body | `string` | yes |
| `first_name` | body | `string` | yes |
| `name` | body | `string` | yes |
| `language` | body | `string` | yes |
| `custom_fields` | body | `object` | no |
