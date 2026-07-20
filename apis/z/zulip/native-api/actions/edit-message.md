# Edit Message with Zulip

Updates an existing message in Zulip.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/messages/:message_id`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Edit Message](https://zulip.com/api/update-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | no | Updated Markdown content for the message. |
| `message_id` | path | `number` | yes | The target message ID. |
| `topic` | body | `string` | no | The new topic for the message thread. |
