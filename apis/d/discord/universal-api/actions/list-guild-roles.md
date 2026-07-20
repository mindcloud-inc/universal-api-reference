# Discord: List Guild Roles

Lists roles in a Discord guild.

```
GET https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-roles?connectionId=$CONNECTION_ID&guildId=123456789012345678" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "123456789012345678"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/list-guild-roles?${params}`, {
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
| `guildId` | string | yes | Target guild ID Example: `123456789012345678`. |

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

Through the native Discord API, this operation is `GET /guilds/:guildId/roles` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guild-roles.md) for the provider-specific parameters and requirements.

