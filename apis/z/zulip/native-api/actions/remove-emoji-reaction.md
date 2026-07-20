# Remove Emoji Reaction with Zulip

Removes an emoji reaction from a Zulip message.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/messages/:message_id/reactions`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Remove Emoji Reaction](https://zulip.com/api/remove-reaction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emoji_name` | body | `string` | yes | The emoji name to remove from the message. |
| `message_id` | path | `number` | yes | The target message ID. |
