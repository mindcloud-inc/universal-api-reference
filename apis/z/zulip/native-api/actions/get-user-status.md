# Get User Status with Zulip

Retrieves a Zulip user's current status details.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/status`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get User Status](https://zulip.com/api/get-user-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_id` | path | `number` | yes | The target user's ID. |
