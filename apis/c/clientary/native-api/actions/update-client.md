# Update Client with Clientary

Updates a client in Clientary by client ID.

## Endpoint

- **Method:** `PUT`
- **Path:** `/clients/:id`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Update Client](https://www.clientary.com/api/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client.number` | body | `string` | no | Optional unique client number. |
| `id` | path | `string` | yes | The Clientary client ID. |
