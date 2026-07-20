# Discord-Bot: Add Guild Member Role

Adds a role to a Discord guild member.

```
POST https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/add-guild-member-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/add-guild-member-role" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guildId": "string",
  "userId": "string",
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/add-guild-member-role', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guildId": "string",
    "userId": "string",
    "roleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guildId` | string | yes | Discord guild (server) ID. |
| `userId` | string | yes | Discord user ID. |
| `roleId` | string | yes | Discord role ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Discord-Bot API returns.

## Native endpoint

Through the native Discord-Bot API, this operation is `PUT /guilds/:guildId/members/:userId/roles/:roleId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-guild-member-role.md) for the provider-specific parameters and requirements.

