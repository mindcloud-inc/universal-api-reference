# Create Contact with SparrowDesk

Creates a contact in SparrowDesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Create Contact](https://developer.sparrowdesk.com/rest-api/endpoints/contacts/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `string` | no | Optional SparrowDesk company identifier. |
| `email` | body | `string` | no | Contact email. Required if phone is not supplied. |
| `first_name` | body | `string` | yes | Contact first name. |
| `last_name` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number. Required if email is not supplied. |
