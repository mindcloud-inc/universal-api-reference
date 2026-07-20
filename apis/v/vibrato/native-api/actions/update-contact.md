# Update contact with Vibrato

Updates an existing contact in Vibrato.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{uuid}/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Update contact](https://docs.getvibrato.com/api-reference/contacts/update-an-existing-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | UUID from Vibrato. |
| `first_name` | body | `string` | yes | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone_number` | body | `string` | no | Phone number. |
| `country_code` | body | `string` | no | Phone country code, for example 1. |
| `tags[]` | body | `array<string>` | no | Tags. |
| `custom_fields[]` | body | `array<object>` | no | Custom fields. |
| `merge_key` | body | `string` | no | Merge key. |
