# Discord: Get Channel

Retrieves a Discord channel by ID.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-channel?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "flags": 1,
      "guildId": "string",
      "iconEmoji": {
        "name": "Ava Chen"
      },
      "id": "string",
      "lastMessageId": "string",
      "name": "Ava Chen",
      "nsfw": true,
      "parentId": "string",
      "permissionOverwrites": [
        {}
      ],
      "position": 1,
      "rateLimitPerUser": 1,
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `flags` | number |  |
| `guildId` | string |  |
| `iconEmoji` | object |  |
| `iconEmoji.name` | string |  |
| `id` | string |  |
| `lastMessageId` | string |  |
| `name` | string |  |
| `nsfw` | boolean |  |
| `parentId` | string |  |
| `permissionOverwrites` | array<object> |  |
| `position` | number |  |
| `rateLimitPerUser` | number |  |
| `type` | number |  |

## Native endpoint

Through the native Discord API, this operation is `GET /channels/:channelId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-channel.md) for the provider-specific parameters and requirements.

