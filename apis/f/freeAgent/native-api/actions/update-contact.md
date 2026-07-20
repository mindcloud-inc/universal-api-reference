# Update Contact with FreeAgent

Updates an existing contact in FreeAgent.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Update Contact](https://dev.freeagent.com/docs/contacts#update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | FreeAgent contact ID. |
| `contact` | body | `object` | no | Contact payload. |
| `contact.first_name` | body | `string` | no | First name. |
| `contact.last_name` | body | `string` | no | Last name. |
| `contact.organisation_name` | body | `string` | no | Organisation name. |
| `contact.email` | body | `string` | no | Email. |
| `contact.phone_number` | body | `string` | no | Telephone. |
