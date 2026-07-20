# Slack: List Message Reactions

Retrieves reactions for an item in Slack.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-reactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-reactions?connectionId=$CONNECTION_ID&channel=string&timestamp=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "timestamp": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-reactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | list<string> | yes | Channel where the message to get reactions for was posted. |
| `timestamp` | list<string> | yes | Timestamp of the message to get reactions for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `full` | boolean | no | If true always return the complete reaction list. |

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
        "permalink": "https://example.com",
        "reactions": [
          {
            "count": 1,
            "name": "Ava Chen",
            "users": [
              "string"
            ]
          }
        ],
        "team": "string",
        "text": "string",
        "ts": "string",
        "type": "string",
        "user": "string"
      },
      "type": "string"
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
| `message.permalink` | string |  |
| `message.reactions[].count` | number |  |
| `message.reactions[].name` | string |  |
| `message.reactions[].users[]` | string |  |
| `message.team` | string |  |
| `message.text` | string |  |
| `message.ts` | string |  |
| `message.type` | string |  |
| `message.user` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET reactions.get` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-reactions.md) for the provider-specific parameters and requirements.

