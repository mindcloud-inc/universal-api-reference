# Create Client with Clientary

Creates a new client in Clientary.

## Endpoint

- **Method:** `POST`
- **Path:** `/clients`
- **Base URL:** `https://{subdomain}.clientary.com/api/v2`
- **Official documentation:** [Create Client](https://www.clientary.com/api/clients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client.name` | body | `string` | yes | The client name. |
| `client.number` | body | `string` | no | Optional unique client number. |
