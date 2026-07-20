# Create User with Zendesk

Creates a new user in Zendesk.

## Endpoint

- **Method:** `POST`
- **Path:** `/users.json`
- **Base URL:** `https://{subdomain}.zendesk.com/api/v2`
- **Official documentation:** [Create User](https://developer.zendesk.com/api-reference/ticketing/users/users/#create-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user.name` | body | `string` | yes | Name for the new user. |
| `user.email` | body | `string` | no | Email for the new user. |
