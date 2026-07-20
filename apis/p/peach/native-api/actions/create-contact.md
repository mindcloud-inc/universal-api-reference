# Create Contact with Peach

Creates a new contact in Peach.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Create Contact](https://peach-organization.gitbook.io/peach/api-reference/contacts/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Contact's first name. |
| `lastName` | body | `string` | yes | Contact's last name. |
| `email` | body | `string` | yes | Contact's email address. |
| `phone` | body | `string` | no | Contact's phone number. |
| `address` | body | `string` | no | Contact address. |
| `city` | body | `string` | no | Contact city. |
| `street` | body | `string` | no | Contact street. |
| `streetNumber` | body | `string` | no | Contact street number. |
| `aptNumber` | body | `string` | no | Contact apartment number. |
| `zipCode` | body | `string` | no | Contact zip code. |
| `groups[]` | body | `array<string>` | no | Group names to add to the contact. |
| `customProperties` | body | `object` | no | Custom properties for the contact. |
