# Update Message with Slack

Updates an existing message in Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `chat.update`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Update Message](https://docs.slack.dev/reference/methods/chat.update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | Channel ID where the message was posted to. |
| `ts` | body | `list` | yes | Timestamp of the message to be updated. |
| `text` | body | `string` | yes | The content of the message. |
| `senderOverride` | body | `list` | no | Override the connection's Default Sender for this action only. Accepted values: `bot`, `user`. Format: `toggle`. |
