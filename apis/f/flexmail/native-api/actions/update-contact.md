# Update Contact with Flexmail

Updates an existing contact in Flexmail.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{id}`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Update Contact](https://api.flexmail.eu/documentation/#patch-/contacts/-id-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `first_name` | body | `string` | no |
| `name` | body | `string` | no |
| `language` | body | `string` | no |
| `custom_fields` | body | `object` | no |
