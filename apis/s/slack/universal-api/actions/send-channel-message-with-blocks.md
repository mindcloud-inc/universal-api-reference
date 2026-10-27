# Slack: Send Channel Message with Blocks



```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-channel-message-with-blocks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-channel-message-with-blocks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "blocks[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/send-channel-message-with-blocks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "blocks[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | yes | Slack channel ID for the message. |
| `blocks[]` | array<object> | yes | Structured Block Kit array. Supply JSON objects, for example section, context, divider, or table blocks. |
| `text` | string | no | Fallback text for notifications and screen readers. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadTimestamp` | string | no | Parent message timestamp when posting a reply. |
| `senderOverride` | list | no | Override the connection's default sender for this action. One of: `bot`, `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "message": {
        "blocks": [
          {}
        ],
        "text": "string",
        "thread_ts": "string"
      },
      "ok": true,
      "ts": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string | Channel ID where the message was posted. |
| `message` | object | Slack message resource. |
| `message.blocks` | array<object> | Structured blocks returned by Slack. |
| `message.text` | string | Fallback message text. |
| `message.thread_ts` | string | Parent message timestamp when this was posted as a reply. |
| `ok` | boolean | Whether Slack accepted the message. |
| `ts` | string | Posted message timestamp and identifier. |

## Native endpoint

Through the native Slack API, this operation is `POST chat.postMessage` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-channel-message-with-blocks.md) for the provider-specific parameters and requirements.

