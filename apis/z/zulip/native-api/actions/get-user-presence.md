# Get User Presence with Zulip

Retrieves a Zulip user's presence information.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id_or_email/presence`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get User Presence](https://zulip.com/api/get-user-presence)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id_or_email` | path | `string` | yes | The target user's ID or email address. |
