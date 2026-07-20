# Update Contact with Clientary

Updates a contact in Clientary by contact ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Contact](https://www.clientary.com/api/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_user.title` | body | `string` | no | The contact title. |
| `id` | path | `string` | no | The Clientary contact ID. |
