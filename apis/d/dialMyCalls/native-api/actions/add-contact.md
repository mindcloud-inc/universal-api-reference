# Add Contact with DialMyCalls

Creates a new contact in DialMyCalls.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact`
- **Base URL:** `https://{apiKey}@api.dialmycalls.com/2.0`
- **Official documentation:** [Add Contact](https://www.dialmycalls.com/api-documentation#contact-add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | The contact's email address. |
| `extension` | body | `string` | no | The contact's phone extension. |
| `extra1` | body | `string` | no | Miscellaneous data about this contact. |
| `firstname` | body | `string` | no | The contact's first name. |
| `groups[]` | body | `array<string>` | no | List of group IDs that this contact should belong to. |
| `lastname` | body | `string` | no | The contact's last name. |
| `phone` | body | `string` | yes | The contact's phone number. |
