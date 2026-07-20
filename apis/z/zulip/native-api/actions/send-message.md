# Send Message with Zulip

Creates a new message in Zulip.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages`
- **Base URL:** `{site}/api/v1`
- **Official documentation:** [Send Message](https://zulip.com/api/send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content` | body | `string` | yes | The Markdown message content to send. |
| `to` | body | `string` | yes | The target channel name, user email, or recipient list, depending on type. |
| `topic` | body | `string` | no | The topic for stream messages. |
| `type` | body | `string` | yes | The Zulip message type, such as stream or private. |
