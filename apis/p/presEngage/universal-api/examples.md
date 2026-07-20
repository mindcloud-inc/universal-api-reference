# PresEngage Universal API Examples

These examples use the MindCloud API key and PresEngage connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves authenticated user details from PresEngage.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/get-authenticated-user?${params}`, {
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
      "email": "ava@example.com",
      "fname": "Ava Chen",
      "lname": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/presEngage/latest/actions/get-authenticated-user).

## Create Webhook Subscription

Creates a new webhook subscription in PresEngage.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/create-webhook-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com/webhook"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presEngage/latest/actions/create-webhook-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com/webhook"
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

See the full [Create Webhook Subscription action reference](actions/create-webhook-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/presEngage/latest/actions/create-webhook-subscription).
