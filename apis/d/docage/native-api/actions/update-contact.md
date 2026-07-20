# Update Contact with Docage

Updates an existing contact in Docage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Contacts/:id`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Update Contact](https://documentation.docage.com/modifier-un-contact-23707612e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | no | The updated contact email address. |
| `FirstName` | body | `string` | no | The updated contact first name. |
| `id` | path | `string` | yes | The Docage contact ID. |
| `LastName` | body | `string` | no | The updated contact last name. |
