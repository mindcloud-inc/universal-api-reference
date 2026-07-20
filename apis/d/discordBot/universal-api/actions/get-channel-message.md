# Discord-Bot: Get Channel Message

Retrieves a specific message from Discord.

```
GET https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel-message?connectionId=$CONNECTION_ID&channelId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-channel-message?${params}`, {
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
| `channelId` | string | yes | Discord channel ID. |
| `messageId` | string | yes | Discord message ID. |

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

Through the native Discord-Bot API, this operation is `GET /channels/:channelId/messages/:messageId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel-message.md) for the provider-specific parameters and requirements.

