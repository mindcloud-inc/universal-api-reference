# Update Client with Timely

Updates an existing client in Timely.

## Endpoint

- **Method:** `PUT`
- **Path:** `/1.1/{account_id}/clients/{id}`
- **Base URL:** `https://api.timelyapp.com`
- **Official documentation:** [Update Client](https://developer.timely.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `number` | yes | Account ID for the client you want to update |
| `id` | path | `number` | yes | Client ID to update |
| `client` | body | `object` | yes | — |
