# Discord-Bot Universal API Examples

These examples use the MindCloud API key and Discord-Bot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current Bot User

Retrieves the current bot user from Discord.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discordBot/latest/actions/get-current-bot-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "bot": true,
      "global_name": "Ava Chen",
      "id": "string",
      "locale": "string",
      "username": "Ava Chen",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [Get Current Bot User action reference](actions/get-current-bot-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discordBot/latest/actions/get-current-bot-user).

## Add Guild Member Role

Adds a role to a Discord guild member.

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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Guild Member Role action reference](actions/add-guild-member-role.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discordBot/latest/actions/add-guild-member-role).
