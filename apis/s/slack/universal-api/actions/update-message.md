# Slack: Update Message

Updates an existing message in Slack.

```
PUT https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channel": "string",
  "ts": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channel": "string",
    "ts": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | list | yes | Channel ID where the message was posted to. |
| `ts` | list | yes | Timestamp of the message to be updated. |
| `text` | string | yes | The content of the message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderOverride` | list | no | Override the connection's Default Sender for this action only. One of: `bot`, `user`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "message": {
        "blocks": [
          {
            "blockId": "string",
            "elements": [
              {
                "elements": [
                  {
                    "text": "string",
                    "type": "string"
                  }
                ],
                "type": "string"
              }
            ],
            "type": "string"
          }
        ],
        "clientMsgId": "string",
        "edited": {
          "ts": "string",
          "user": "string"
        },
        "team": "string",
        "text": "string",
        "type": "string",
        "user": "string"
      },
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `message.blocks[].blockId` | string |  |
| `message.blocks[].elements[].elements[].text` | string |  |
| `message.blocks[].elements[].elements[].type` | string |  |
| `message.blocks[].elements[].type` | string |  |
| `message.blocks[].type` | string |  |
| `message.clientMsgId` | string |  |
| `message.edited.ts` | string |  |
| `message.edited.user` | string |  |
| `message.team` | string |  |
| `message.text` | string |  |
| `message.type` | string |  |
| `message.user` | string |  |
| `text` | string |  |

## Native endpoint

Through the native Slack API, this operation is `POST chat.update` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

