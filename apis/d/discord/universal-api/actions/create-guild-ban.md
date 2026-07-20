# Discord: Create Guild Ban

Creates a guild ban in Discord.

```
POST https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-guild-ban
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-guild-ban" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "123456789012345678",
  "userId": "123456789012345678"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discord/latest/actions/create-guild-ban', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "123456789012345678",
    "userId": "123456789012345678"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | Target guild ID Example: `123456789012345678`. |
| `userId` | string | yes | User ID to ban Example: `123456789012345678`. |
| `deleteMessageSeconds` | number | no | Delete message history in seconds (0-604800) Example: `3600`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deleteMessageDays` | number | no | Deprecated delete window in days (0-7) Example: `7`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Empty response body on success. |

## Native endpoint

Through the native Discord API, this operation is `PUT /guilds/:guildId/bans/:userId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-guild-ban.md) for the provider-specific parameters and requirements.

