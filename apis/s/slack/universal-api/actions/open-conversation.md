# Slack: Open Conversation

Opens or resumes a direct conversation in Slack.

```
POST https://connect.mindcloud.co/v1/universal/slack/latest/actions/open-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Slack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/slack/latest/actions/open-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/slack/latest/actions/open-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `users` | list<string> | yes | Comma separated lists of users. If only one user is included, this creates a 1:1 DM. The ordering of the users is preserved whenever a multi-person direct message is returned. Supply a channel when not supplying users. Accepts multiple values in one string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | list<string> | no | Resume a conversation by supplying an im or mpim's ID. Or provide the users field instead. |
| `preventCreation` | boolean | no | Do not create a direct message or multi-person direct message. This is used to see if there is an existing dm or mpdm. |
| `returnIM` | boolean | no | Indicates you want the full conversation object in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alreadyOpen": true,
      "channel": {
        "contextTeamId": "string",
        "created": 1,
        "id": "string",
        "isArchived": true,
        "isIm": true,
        "isOpen": true,
        "isOrgShared": true,
        "lastRead": "string",
        "latest": {
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
          "team": "string",
          "text": "string",
          "ts": "string",
          "type": "string",
          "user": "string"
        },
        "priority": 1,
        "properties": {
          "tabs": [
            {
              "id": "string",
              "label": "string",
              "type": "string"
            }
          ],
          "tabz": [
            {
              "type": "string"
            }
          ]
        },
        "unreadCount": 1,
        "unreadCountDisplay": 1,
        "updated": 1,
        "user": "string"
      },
      "noOp": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alreadyOpen` | boolean |  |
| `channel.contextTeamId` | string |  |
| `channel.created` | number |  |
| `channel.id` | string |  |
| `channel.isArchived` | boolean |  |
| `channel.isIm` | boolean |  |
| `channel.isOpen` | boolean |  |
| `channel.isOrgShared` | boolean |  |
| `channel.lastRead` | string |  |
| `channel.latest.blocks[].blockId` | string |  |
| `channel.latest.blocks[].elements[].elements[].text` | string |  |
| `channel.latest.blocks[].elements[].elements[].type` | string |  |
| `channel.latest.blocks[].elements[].type` | string |  |
| `channel.latest.blocks[].type` | string |  |
| `channel.latest.clientMsgId` | string |  |
| `channel.latest.team` | string |  |
| `channel.latest.text` | string |  |
| `channel.latest.ts` | string |  |
| `channel.latest.type` | string |  |
| `channel.latest.user` | string |  |
| `channel.priority` | number |  |
| `channel.properties.tabs[].id` | string |  |
| `channel.properties.tabs[].label` | string |  |
| `channel.properties.tabs[].type` | string |  |
| `channel.properties.tabz[].type` | string |  |
| `channel.unreadCount` | number |  |
| `channel.unreadCountDisplay` | number |  |
| `channel.updated` | number |  |
| `channel.user` | string |  |
| `noOp` | boolean |  |

## Native endpoint

Through the native Slack API, this operation is `POST conversations.open` (base URL `https://slack.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/open-conversation.md) for the provider-specific parameters and requirements.

