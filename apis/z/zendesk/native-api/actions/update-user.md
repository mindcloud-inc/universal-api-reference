# Update User with Zendesk

Updates an existing user in Zendesk.

## Endpoint

- **Method:** `PUT`
- **Path:** `/users/:id.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Update User](https://developer.zendesk.com/api-reference/ticketing/users/users/#update-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Zendesk user ID. |
| `user.name` | body | `string` | no | Updated user name. |
| `user.email` | body | `string` | no | Updated user email. |
