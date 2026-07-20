# Scoreboard Buzz Universal API Examples

These examples use the MindCloud API key and Scoreboard Buzz connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from Scoreboard Buzz.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/list-users?${params}`, {
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
      "id": 1,
      "user_email": "ava@example.com",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scoreboardBuzz/latest/actions/list-users).

## Create Webhook Subscription

Creates a webhook subscription in Scoreboard Buzz.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scoreboardBuzz/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com"
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
      "account_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "event_type": "string",
      "id": 1,
      "status": 1,
      "target_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook Subscription action reference](actions/create-webhook-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scoreboardBuzz/latest/actions/create-webhook-subscription).
