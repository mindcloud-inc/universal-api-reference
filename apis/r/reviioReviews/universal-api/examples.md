# Revi.io Reviews Universal API Examples

These examples use the MindCloud API key and Revi.io Reviews connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Hello World

Tests the Revi.io Reviews API connection.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world?connectionId=$CONNECTION_ID&test=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "test": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/hello-world?${params}`, {
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
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Hello World action reference](actions/hello-world.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reviioReviews/latest/actions/hello-world).

## Create Orders

Creates orders in Revi.io Reviews.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/create-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reviioReviews/latest/actions/create-orders', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}]
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
      "orders_count": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Orders action reference](actions/create-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/reviioReviews/latest/actions/create-orders).
