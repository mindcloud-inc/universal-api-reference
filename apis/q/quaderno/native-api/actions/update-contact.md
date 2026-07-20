# Update Contact with Quaderno

Updates an existing contact in Quaderno.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [Update Contact](https://developers.quaderno.io/api/#tag/Contacts/operation/updateContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `city` | body | `string` | no | Updated city. |
| `country` | body | `string` | no | Updated country. |
| `email` | body | `string` | no | Updated email address. |
| `first_name` | body | `string` | no | Updated first name. |
| `id` | path | `string` | yes | ID of the contact to update. |
| `notes` | body | `string` | no | Updated notes. |
| `postal_code` | body | `string` | no | Updated postal code. |
| `region` | body | `string` | no | Updated region. |
| `street_line_1` | body | `string` | no | Updated primary street address. |
