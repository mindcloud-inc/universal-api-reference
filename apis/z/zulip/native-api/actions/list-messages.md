# List Messages with Zulip

Retrieves messages from Zulip using specified filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [List Messages](https://zulip.com/api/get-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `anchor` | query | `string` | no | Where to anchor the message query, for example newest or a message ID. |
| `num_after` | query | `number` | no | How many messages to return after the anchor. |
| `num_before` | query | `number` | no | How many messages to return before the anchor. |
