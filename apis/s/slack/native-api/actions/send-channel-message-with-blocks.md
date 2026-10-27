# Send Channel Message with Blocks with Slack

## Endpoint

- **Method:** `POST`
- **Path:** `chat.postMessage`
- **Base URL:** `https://slack.com/api/`
- **Official documentation:** [Send Channel Message with Blocks](https://docs.slack.dev/reference/methods/chat.postMessage/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel` | body | `string` | yes | Slack channel ID for the message. |
| `blocks[]` | body | `array<object>` | yes | Structured Block Kit array. Supply JSON objects, for example section, context, divider, or table blocks. |
| `text` | body | `string` | no | Fallback text for notifications and screen readers. |
| `thread_ts` | body | `string` | no | Parent message timestamp when posting a reply. |
| `senderOverride` | body | `list` | no | Override the connection's default sender for this action. Accepted values: `bot`, `user`. |
