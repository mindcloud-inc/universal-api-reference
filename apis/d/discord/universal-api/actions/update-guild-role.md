# Discord: Update Guild Role

Updates a role in a Discord guild.

```
PUT https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "123456789012345678",
  "roleId": "123456789012345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/update-guild-role', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "123456789012345678",
    "roleId": "123456789012345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | Target guild ID Example: `123456789012345678`. |
| `roleId` | string | yes | Role ID to update Example: `123456789012345678`. |
| `name` | string | no | Role name (max 100 chars) Example: `Moderators`. |
| `permissions` | string | no | Bitwise permissions string Example: `104324673`. |
| `colors` | object | no | Role colors object |
| `hoist` | boolean | no | Display role separately Example: `false`. |
| `icon` | string | no | Role icon image data |
| `unicodeEmoji` | string | no | Role unicode emoji Example: `🛡️`. |
| `mentionable` | boolean | no | Whether role is mentionable Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `color` | number | no | Deprecated RGB color integer Example: `3447003`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": 1,
      "colors": {},
      "flags": 1,
      "hoist": true,
      "icon": "string",
      "id": "string",
      "managed": true,
      "mentionable": true,
      "name": "Ava Chen",
      "permissions": "string",
      "position": 1,
      "unicodeEmoji": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | number |  |
| `colors` | object |  |
| `flags` | number |  |
| `hoist` | boolean |  |
| `icon` | string |  |
| `id` | string |  |
| `managed` | boolean |  |
| `mentionable` | boolean |  |
| `name` | string |  |
| `permissions` | string |  |
| `position` | number |  |
| `unicodeEmoji` | string |  |

## Native endpoint

Through the native Discord API, this operation is `PATCH /guilds/:guildId/roles/:roleId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-guild-role.md) for the provider-specific parameters and requirements.

