# Slack: Schedule Message

Creates a scheduled message in Slack.

```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/schedule-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/schedule-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "text": "string",
  "postAt": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/schedule-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "text": "string",
    "postAt": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | list | yes | Channel to send the message to. |
| `text` | string | yes | The content of the message. |
| `postAt` | date | yes | Unix timestamp representing the future time the message should post to Slack. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `unfurlLinks` | boolean | no | Pass true to enable unfurling of primarily text-based content. Default: `true`. |
| `unfurlMedia` | boolean | no | Pass false to disable unfurling of media content. Default: `true`. |
| `parse` | list | no | By default, URLs will be hyperlinked. Set parse to none to remove the hyperlinks. The behavior of parse is different for text formatted with markdown. By default, or when parse is set to none, markdown formatting is implemented. To ignore markdown formatting, set parse to full. |
| `threadTimestamp` | list | no | Provide another message's timestamp value to make this message a reply. Avoid using a reply's timestamp value; use its parent instead. |
| `replyBroadcast` | boolean | no | Used in conjunction with Thread Timestamp and indicates whether reply should be made visible to everyone in the channel or conversation. |
| `senderOverride` | list | no | Override the connection's Default Sender for this action only. One of: `bot`, `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "message": {
        "attachments": [
          {
            "fallback": "string",
            "id": 1,
            "text": "string"
          }
        ],
        "botId": "string",
        "subtype": "string",
        "text": "string",
        "type": "string",
        "username": "Ava Chen"
      },
      "postAt": "string",
      "scheduledMessageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `message.attachments[].fallback` | string |  |
| `message.attachments[].id` | number |  |
| `message.attachments[].text` | string |  |
| `message.botId` | string |  |
| `message.subtype` | string |  |
| `message.text` | string |  |
| `message.type` | string |  |
| `message.username` | string |  |
| `postAt` | string |  |
| `scheduledMessageId` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST chat.scheduleMessage` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-message.md) for the provider-specific parameters and requirements.

