# BotHunter Universal API Examples

These examples use the MindCloud API key and BotHunter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Community Variable

Retrieves a BotHunter community variable value.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/get-community-variable?connectionId=$CONNECTION_ID&varId=607d97c6a01c6a25972ed95e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "varId": "607d97c6a01c6a25972ed95e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/get-community-variable?${params}`, {
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
      "value": "string",
      "varId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Community Variable action reference](actions/get-community-variable.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botHunter/latest/actions/get-community-variable).

## Add User To Bot

Creates a BotHunter bot enrollment for a user in a specified channel.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/add-user-to-bot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": "607d97c6a01c6a25972ed95e",
  "uid": "102036383",
  "channel": "VK"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHunter/latest/actions/add-user-to-bot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": "607d97c6a01c6a25972ed95e",
    "uid": "102036383",
    "channel": "VK"
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
      "botId": "string",
      "channel": "string",
      "message": "string",
      "success": true,
      "uid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add User To Bot action reference](actions/add-user-to-bot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botHunter/latest/actions/add-user-to-bot).
