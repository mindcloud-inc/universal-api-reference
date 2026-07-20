# Delete Message with Slack

Deletes an existing message from Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `chat.delete`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Delete Message](https://docs.slack.dev/reference/methods/chat.delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | Channel containing the message to be deleted. |
| `ts` | body | `list` | yes | Timestamp of the message to be deleted. |
| `senderOverride` | body | `list` | no | Override the connection's Default Sender for this action only. Accepted values: `bot`, `user`. Format: `toggle`. |
