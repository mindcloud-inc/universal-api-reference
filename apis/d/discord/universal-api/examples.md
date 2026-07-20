# Discord Universal API Examples

These examples use the MindCloud API key and Discord connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current authenticated Discord user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/discord/latest/actions/get-current-user?${params}`, {
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
      "accentColor": 1,
      "avatar": "string",
      "avatarDecorationData": {},
      "banner": "string",
      "bannerColor": "string",
      "clan": {},
      "collectibles": {},
      "discriminator": "string",
      "displayNameStyles": {},
      "flags": 1,
      "globalName": "Ava Chen",
      "id": "string",
      "locale": "string",
      "mfaEnabled": true,
      "premiumType": 1,
      "primaryGuild": {},
      "publicFlags": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discord/latest/actions/get-current-user).

## Create Guild Ban

Creates a guild ban in Discord.

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

Example response:

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

See the full [Create Guild Ban action reference](actions/create-guild-ban.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/discord/latest/actions/create-guild-ban).
