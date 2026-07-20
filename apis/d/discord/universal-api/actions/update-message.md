# Discord: Update Message

Updates a message in a Discord channel.

```
PUT https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "123456789012345678",
  "messageId": "123456789012345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "123456789012345678",
    "messageId": "123456789012345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channelId` | string | yes | Channel identifier. Example: `123456789012345678`. |
| `messageId` | string | yes | Message identifier. Example: `123456789012345678`. |
| `content` | string | no | Updated message text content. Example: `Updated message content`. |
| `embeds[]` | array<object> | no | Updated embeds array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `components[]` | array<object> | no | Updated message components. |
| `attachments[]` | array<object> | no | Updated attachment objects. |
| `allowedMentions` | object | no | Controls mention parsing for edited content. |
| `flags` | number | no | Message flags bitfield. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "author": {
        "avatar": "string",
        "bot": true,
        "discriminator": "string",
        "flags": 1,
        "id": "string",
        "publicFlags": 1,
        "username": "Ava Chen"
      },
      "channelId": "string",
      "components": [
        {}
      ],
      "content": "string",
      "editedTimestamp": "2026-05-07T12:00:00.000Z",
      "embeds": [
        {}
      ],
      "flags": 1,
      "id": "string",
      "mentionEveryone": true,
      "mentionRoles": [
        "string"
      ],
      "mentions": [
        {}
      ],
      "pinned": true,
      "timestamp": "2026-05-07T12:00:00.000Z",
      "tts": true,
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
| `author.avatar` | string |  |
| `author.bot` | boolean |  |
| `author.discriminator` | string |  |
| `author.flags` | number |  |
| `author.id` | string |  |
| `author.publicFlags` | number |  |
| `author.username` | string |  |
| `channelId` | string |  |
| `components` | array<object> |  |
| `content` | string |  |
| `editedTimestamp` | date |  |
| `embeds` | array<object> |  |
| `flags` | number |  |
| `id` | string |  |
| `mentionEveryone` | boolean |  |
| `mentionRoles` | array<string> |  |
| `mentions` | array<object> |  |
| `pinned` | boolean |  |
| `timestamp` | date |  |
| `tts` | boolean |  |
| `type` | number |  |

## Native endpoint

Through the native Discord API, this operation is `PATCH /channels/:channelId/messages/:messageId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.

