# Create Contact with Nutshell

Creates a new contact in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Create Contact](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contacts[].name` | body | `string` | no | Full name for the contact. |
| `contacts[].description` | body | `string` | no | Description to show under the contact name. |
| `contacts[].emails[].value` | body | `string` | no | Email address for the contact. |
| `contacts[].phones[].value.countryCode` | body | `string` | no | Country code for the contact phone number. |
| `contacts[].phones[].value.number` | body | `string` | no | Phone number digits for the contact. |
| `contacts[].links.accounts[]` | body | `array<string>` | no | Company IDs to associate with the contact. Send multiple values as a array. |
| `contacts[].links.owner` | body | `string` | no | Owner user ID for the contact. |
