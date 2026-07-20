# Update Contact with Peach

Updates an existing contact in Peach.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updateContact/:contactId`
- **Base URL:** `https://api.peach-in.com/v4`
- **Official documentation:** [Update Contact](https://peach-organization.gitbook.io/peach/api-reference/contacts/update-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The contact ID to update. |
| `firstName` | body | `string` | no | Contact's first name. |
| `lastName` | body | `string` | no | Contact's last name. |
| `email` | body | `string` | no | Contact's email address. |
| `phone` | body | `string` | no | Contact's phone number. |
| `address` | body | `string` | no | Contact address. |
| `city` | body | `string` | no | Contact city. |
| `street` | body | `string` | no | Contact street. |
| `streetNumber` | body | `string` | no | Contact street number. |
| `aptNumber` | body | `string` | no | Contact apartment number. |
| `zipCode` | body | `string` | no | Contact zip code. |
| `groups[]` | body | `array<string>` | no | Group names to add to the contact. |
| `removeGroups[]` | body | `array<string>` | no | Group names to remove from the contact. |
| `customProperties` | body | `object` | no | Custom properties for the contact. |
