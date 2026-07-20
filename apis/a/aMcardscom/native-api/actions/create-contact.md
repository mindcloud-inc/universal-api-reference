# Create Contact with AMcards.com

Creates a new contact in AMcards.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [Create Contact](https://staging.amcards.com/docs/developers-only/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_line_1` | body | `string` | no | Primary street address for the contact. |
| `address_line_2` | body | `string` | no | Secondary address line for apartment, suite, or unit. |
| `birth_day` | body | `string` | no | Birth day value used for AMcards reminder/contact data. |
| `birth_month` | body | `string` | no | Birth month value used for AMcards reminder/contact data. |
| `birth_year` | body | `string` | no | Birth year value used for AMcards reminder/contact data. |
| `city` | body | `string` | no | City for the contact mailing address. |
| `country` | body | `string` | no | Two-letter country code for the contact mailing address. |
| `email_address` | body | `string` | no | Email address for the contact. |
| `first_name` | body | `string` | no | First name for the contact. |
| `groups[]` | body | `array<string>` | yes | List of AMcards group resource URIs. Use an empty list when the contact should not be assigned to a group. |
| `last_name` | body | `string` | no | Last name for the contact. |
| `notes` | body | `string` | no | Freeform note stored on the AMcards contact. |
| `owner` | body | `string` | no | AMcards owner resource URI such as `/.api/v1/user/47054/`. |
| `phone_number` | body | `string` | no | Phone number for the contact. |
| `postal_code` | body | `string` | no | Postal code for the contact mailing address. |
| `state` | body | `string` | no | State or province for the contact mailing address. |
