# Botbaba Universal API Examples

These examples use the MindCloud API key and Botbaba connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/list-bots?${params}`, {
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
      "botName": "Ava Chen",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botbaba/latest/actions/list-bots).

## Create Bot User



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-bot-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botbaba/latest/actions/create-bot-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "name": "Ava Chen"
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
      "botUserId": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Bot User action reference](actions/create-bot-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botbaba/latest/actions/create-bot-user).
