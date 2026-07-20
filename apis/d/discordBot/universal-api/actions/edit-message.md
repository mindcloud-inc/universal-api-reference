# Discord-Bot: Edit Message

Updates an existing message in Discord.

```
PUT https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/edit-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/edit-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "string",
  "messageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/edit-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "string",
    "messageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Discord channel ID. |
| `messageId` | string | yes | Discord message ID. |
| `content` | string | no | New message content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "author": {},
      "channel_id": "string",
      "content": "string",
      "edited_timestamp": "2026-05-07T12:00:00.000Z",
      "embeds": [
        {}
      ],
      "id": "string",
      "pinned": true,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `author` | object |  |
| `channel_id` | string |  |
| `content` | string |  |
| `edited_timestamp` | date |  |
| `embeds` | array<object> |  |
| `id` | string |  |
| `pinned` | boolean |  |
| `timestamp` | date |  |
| `type` | number |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `PATCH /channels/:channelId/messages/:messageId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/edit-message.md) for the provider-specific parameters and requirements.

