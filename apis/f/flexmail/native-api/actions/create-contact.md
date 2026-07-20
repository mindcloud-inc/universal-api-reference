# Create Contact with Flexmail

Creates a new contact in Flexmail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [Create Contact](https://api.flexmail.eu/documentation/#post-/contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `language` | body | `string` | yes |
| `source` | body | `number` | yes |
| `first_name` | body | `string` | no |
| `name` | body | `string` | no |
| `custom_fields` | body | `object` | no |
