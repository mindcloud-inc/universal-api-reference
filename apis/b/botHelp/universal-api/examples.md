# BotHelp Universal API Examples

These examples use the MindCloud API key and BotHelp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bots

Retrieves active bot details from BotHelp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/list-bots?${params}`, {
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
      "referral": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Bots action reference](actions/list-bots.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botHelp/latest/actions/list-bots).

## Add Messenger Subscriber To Funnel

Adds a subscriber to a funnel by Facebook Messenger user ID in BotHelp.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/add-messenger-subscriber-to-funnel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "funnelReferral": "string",
  "messenger_user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/botHelp/latest/actions/add-messenger-subscriber-to-funnel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "funnelReferral": "string",
    "messenger_user_id": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Messenger Subscriber To Funnel action reference](actions/add-messenger-subscriber-to-funnel.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/botHelp/latest/actions/add-messenger-subscriber-to-funnel).
