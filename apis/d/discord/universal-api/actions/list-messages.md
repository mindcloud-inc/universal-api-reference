# Discord: List Messages

Lists messages in a Discord channel.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-messages?${params}`, {
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
| `channelId` | string | yes | Channel identifier. Example: `123456789012345678`. |
| `limit` | number | no | Maximum number of messages to return (1-100). Example: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `around` | string | no | Get messages around this message ID. Example: `123456789012345678`. |
| `before` | string | no | Get messages before this message ID. Example: `123456789012345678`. |
| `after` | string | no | Get messages after this message ID. Example: `123456789012345678`. |

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

Through the native Discord API, this operation is `GET /channels/:channelId/messages` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.

