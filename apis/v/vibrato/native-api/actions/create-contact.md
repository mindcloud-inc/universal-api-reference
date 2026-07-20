# Create contact with Vibrato

Creates a new contact in Vibrato.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/`
- **Base URL:** `https://api.getvibrato.com/api/v1`
- **Official documentation:** [Create contact](https://docs.getvibrato.com/api-reference/contacts/create-a-new-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone_number` | body | `string` | no | Phone number. |
| `country_code` | body | `string` | no | Phone country code, for example 1. |
| `tags[]` | body | `array<string>` | no | Tags. |
| `custom_fields[]` | body | `array<object>` | no | Custom fields. |
| `merge_key` | body | `string` | no | Merge key. |
