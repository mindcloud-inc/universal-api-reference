# Get User with Zulip

Retrieves a specific Zulip user by ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get User](https://zulip.com/api/get-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The target user's ID. |
