# Get User by Email with Zulip

Retrieves a specific Zulip user by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:email`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get User by Email](https://zulip.com/api/get-user-by-email)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | path | `string` | yes | The target user's Zulip API email address. |
