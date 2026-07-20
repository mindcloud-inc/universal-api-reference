# Create Contact with Clientary

Creates a new contact for a client in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/:client_id/contacts`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Contact](https://www.clientary.com/api/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | path | `string` | yes | The parent client ID. |
| `client_user.email` | body | `string` | yes | The contact email address. |
| `client_user.name` | body | `string` | yes | The contact name. |
