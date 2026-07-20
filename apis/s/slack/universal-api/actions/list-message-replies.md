# Slack: List Message Replies

Retrieves replies from a Slack conversation thread.

```
GET https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-replies?connectionId=$CONNECTION_ID&channel=string&ts=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channel": "string",
  "ts": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/slack/latest/actions/list-message-replies?${params}`, {
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
| `channel` | list<string> | yes | Conversation ID to fetch thread from. |
| `ts` | list<string> | yes | Unique identifier of either a thread’s parent message or a message in the thread. ts must be the timestamp of an existing message with 0 or more replies. If there are no replies then just the single message referenced by ts will return - it is just an ordinary, unthreaded message. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeAllMetadata` | boolean<string> | no | Return all metadata associated with this message. |
| `inclusive` | boolean | no | Include messages with oldest or latest timestamps in results. Ignored unless either timestamp is specified. |
| `latest` | date | no | Only messages before this Unix timestamp will be included in results. |
| `oldest` | date | no | Only messages after this Unix timestamp will be included in results. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
      "isLocked": true,
      "lastRead": "string",
      "latestReply": "string",
      "reactions": [
        {
          "count": 1,
          "name": "Ava Chen",
          "users": [
            "string"
          ]
        }
      ],
      "replyCount": 1,
      "replyUsers": [
        "string"
      ],
      "replyUsersCount": 1,
      "subscribed": true,
      "team": "string",
      "text": "string",
      "threadTs": "string",
      "ts": "string",
      "type": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocks[].blockId` | string |  |
| `blocks[].elements[].elements[].text` | string |  |
| `blocks[].elements[].elements[].type` | string |  |
| `blocks[].elements[].type` | string |  |
| `blocks[].type` | string |  |
| `clientMsgId` | string |  |
| `edited.ts` | string |  |
| `edited.user` | string |  |
| `isLocked` | boolean |  |
| `lastRead` | string |  |
| `latestReply` | string |  |
| `reactions[].count` | number |  |
| `reactions[].name` | string |  |
| `reactions[].users[]` | string |  |
| `replyCount` | number |  |
| `replyUsers[]` | string |  |
| `replyUsersCount` | number |  |
| `subscribed` | boolean |  |
| `team` | string |  |
| `text` | string |  |
| `threadTs` | string |  |
| `ts` | string |  |
| `type` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Slack API, this operation is `GET conversations.replies` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-message-replies.md) for the provider-specific parameters and requirements.

