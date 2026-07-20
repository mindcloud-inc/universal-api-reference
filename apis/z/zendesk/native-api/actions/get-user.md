# Get User with Zendesk

Retrieves a user from Zendesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Get User](https://developer.zendesk.com/api-reference/ticketing/users/users/#show-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk user ID. |
