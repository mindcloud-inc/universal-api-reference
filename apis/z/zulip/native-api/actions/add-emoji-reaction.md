# Add Emoji Reaction with Zulip

Adds an emoji reaction to a Zulip message.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/:message_id/reactions`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Add Emoji Reaction](https://zulip.com/api/add-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emoji_name` | body | `string` | yes | The emoji name to add as a reaction. |
| `message_id` | path | `number` | yes | The target message ID. |
