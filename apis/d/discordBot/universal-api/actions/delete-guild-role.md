# Discord-Bot: Delete Guild Role

Deletes a role from a Discord guild.

```
DELETE https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-guild-role
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Discord-Bot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-guild-role?connectionId=$CONNECTION_ID&guildId=string&roleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guildId": "string",
  "roleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/delete-guild-role?${params}`, {
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
| `guildId` | string | yes | Discord guild (server) ID. |
| `roleId` | string | yes | Discord role ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Discord-Bot API returns.

## Native endpoint

Through the native Discord-Bot API, this operation is `DELETE /guilds/:guildId/roles/:roleId` (base URL `https://discord.com/api/v10`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-guild-role.md) for the provider-specific parameters and requirements.

