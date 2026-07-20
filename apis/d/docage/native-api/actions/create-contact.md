# Create Contact with Docage

Creates a new contact in Docage.

## Endpoint

- **Method:** `POST`
- **Path:** `/Contacts`
- **Base URL:** `https://api.docage.com`
- **Official documentation:** [Create Contact](https://documentation.docage.com/cr%C3%A9er-un-contact-23707615e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Email` | body | `string` | no | The contact email address. |
| `FirstName` | body | `string` | no | The contact first name. |
| `LastName` | body | `string` | yes | The contact last name. |
