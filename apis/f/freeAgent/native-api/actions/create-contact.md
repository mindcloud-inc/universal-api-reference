# Create Contact with FreeAgent

Creates a new contact in FreeAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [Create Contact](https://dev.freeagent.com/docs/contacts#create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | no | Contact payload. |
| `contact.first_name` | body | `string` | no | First name. |
| `contact.last_name` | body | `string` | no | Last name. |
| `contact.organisation_name` | body | `string` | no | Organisation name. |
| `contact.email` | body | `string` | no | Email. |
| `contact.phone_number` | body | `string` | no | Telephone. |
