# Discord-Bot: Create Guild Role

Creates a role in a Discord guild.

```
POST https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/create-guild-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | Discord guild (server) ID. |
| `name` | string | no | Role name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": 1,
      "id": "string",
      "managed": true,
      "mentionable": true,
      "name": "Ava Chen",
      "permissions": "string",
      "position": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | number |  |
| `id` | string |  |
| `managed` | boolean |  |
| `mentionable` | boolean |  |
| `name` | string |  |
| `permissions` | string |  |
| `position` | number |  |

## Native endpoint

Through the native Discord-Bot API, this operation is `POST /guilds/:guildId/roles` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-guild-role.md) for the provider-specific parameters and requirements.

