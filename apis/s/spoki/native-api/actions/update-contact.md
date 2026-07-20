# Update Contact with Spoki

Updates a contact by ID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/{{id}}/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Update Contact](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The contact ID. |
| `phone` | body | `string` | yes | The contact phone number. Include the current phone number when updating a contact. |
| `first_name` | body | `string` | no | The contact first name. |
| `last_name` | body | `string` | no | The contact last name. |
| `email` | body | `string` | no | The contact email address. |
| `language` | body | `string` | no | The contact language code. |
| `custom_fields` | body | `object` | no | Custom fields keyed by Spoki field code. |
