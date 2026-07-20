# Delete Scheduled Message with Slack

Deletes a scheduled message from Slack.

## Endpoint

- **Method:** `POST`
- **Path:** `chat.deleteScheduledMessage`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Delete Scheduled Message](https://docs.slack.dev/reference/methods/chat.deleteScheduledMessage/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `list` | yes | The channel the message will be posted to |
| `scheduled_message_id` | body | `list` | yes | ID of the scheduled message |
| `senderOverride` | body | `list` | no | Override the connection's Default Sender for this action only. Accepted values: `bot`, `user`. Format: `toggle`. |
