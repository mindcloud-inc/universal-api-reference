# Discord-Bot: Create Guild Channel

Creates a channel in a Discord guild.

```
POST https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-channel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-channel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-channel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | Discord guild (server) ID. |
| `name` | string | yes | Channel name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guild_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "nsfw": true,
      "parent_id": "string",
      "position": 1,
      "topic": "string",
      "type": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guild_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `nsfw` | boolean |  |
| `parent_id` | string |  |
| `position` | number |  |
| `topic` | string |  |
| `type` | number |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `POST /guilds/:guildId/channels` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-guild-channel.md) for the provider-specific parameters and requirements.

