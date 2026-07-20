# Invidious Universal API Examples

These examples use the MindCloud API key and Invidious connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Stats



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats?${params}`, {
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
      "metadata": {
        "updatedAt": 1
      },
      "openRegistrations": true,
      "software": {
        "name": "Ava Chen",
        "version": "string"
      },
      "usage": {
        "users": {
          "activeHalfyear": 1,
          "total": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Stats action reference](actions/get-stats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invidious/latest/actions/get-stats).

## Add Auth Subscription



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-auth-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invidious/latest/actions/add-auth-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "channelId": "UC_x5XG1OV2P6uZZ5FSM9Ttw"
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
      "authorId": "string",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Auth Subscription action reference](actions/add-auth-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invidious/latest/actions/add-auth-subscription).
