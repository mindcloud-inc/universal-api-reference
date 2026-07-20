# Create Client Contact with Timizer

Creates a client contact in Timizer.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/clients/:id/contacts`
- **Base URL:** `https://api.timizer.io`
- **Official documentation:** [Create Client Contact](https://api-doc.timizer.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Email address of the contact. |
| `firstname` | body | `string` | no | First name of the contact. |
| `id` | path | `number` | yes | ID of the client. |
| `lastname` | body | `string` | no | Last name of the contact. |
| `occupation` | body | `string` | no | Occupation of the contact. |
