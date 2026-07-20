# Get Subscription Status with Zulip

Retrieves a user's subscription status for a Zulip channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/:user_id/subscriptions/:stream_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Get Subscription Status](https://zulip.com/api/get-subscription-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stream_id` | path | `number` | yes | The target channel ID. |
| `user_id` | path | `number` | yes | The target user's ID. |
