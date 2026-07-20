# Delete User with Zendesk

Deletes an existing user from Zendesk.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/users/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Delete User](https://developer.zendesk.com/api-reference/ticketing/users/users/#delete-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk user ID. |
