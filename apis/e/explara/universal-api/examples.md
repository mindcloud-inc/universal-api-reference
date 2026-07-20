# Explara Universal API Examples

These examples use the MindCloud API key and Explara connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Account Profile

Retrieves an account profile from Explara.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/explara/latest/actions/account-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/explara/latest/actions/account-profile?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Account Profile action reference](actions/account-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/explara/latest/actions/account-profile).

## Event Generate Order

Creates a new event order in Explara.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/explara/latest/actions/event-generate-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventId": "string",
  "tickets[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/explara/latest/actions/event-generate-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventId": "string",
    "tickets[]": [{}]
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

See the full [Event Generate Order action reference](actions/event-generate-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/explara/latest/actions/event-generate-order).
