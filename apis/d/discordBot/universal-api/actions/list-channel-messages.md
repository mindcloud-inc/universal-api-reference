# Discord-Bot: List Channel Messages

Retrieves messages from a Discord channel.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-channel-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-channel-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/list-channel-messages?${params}`, {
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
| `after` | string | no | Return messages after this message ID. |
| `around` | string | no | Return messages around this message ID. Do not combine with before or after. |
| `channelId` | string | yes | Discord channel ID. |

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

Through the native Discord-Bot API, this operation is `GET /channels/:channelId/messages` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-channel-messages.md) for the provider-specific parameters and requirements.

