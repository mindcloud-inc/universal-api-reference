# Discord: List Guild Channels

Lists channels in a Discord guild.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-channels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-channels?connectionId=$CONNECTION_ID&guildId=123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-channels?${params}`, {
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
| `guildId` | string | yes | Guild identifier. Example: `123456789012345678`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bitrate": 1,
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
      "type": 1,
      "userLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bitrate` | number |  |
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
| `userLimit` | number |  |

## Native endpoint

Through the native Discord API, this operation is `GET /guilds/:guildId/channels` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guild-channels.md) for the provider-specific parameters and requirements.

