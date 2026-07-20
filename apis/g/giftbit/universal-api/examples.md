# Giftbit Universal API Examples

These examples use the MindCloud API key and Giftbit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Ping

Tests your Giftbit authentication and API health.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/ping?${params}`, {
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
      "displayname": "Ava Chen",
      "info": {},
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Ping action reference](actions/ping.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giftbit/latest/actions/ping).

## Create Campaign Order

Creates a Giftbit campaign order for emailed or shortlink rewards.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/create-campaign-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "priceInCents": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/create-campaign-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "priceInCents": 1
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
      "campaign": {},
      "info": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign Order action reference](actions/create-campaign-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/giftbit/latest/actions/create-campaign-order).
