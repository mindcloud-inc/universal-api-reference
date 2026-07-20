# CoinGate Universal API Examples

These examples use the MindCloud API key and CoinGate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Retrieves orders from your CoinGate account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/list-orders?${params}`, {
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
      "currentPage": 1,
      "orders": [
        {
          "id": 1
        }
      ],
      "perPage": 1,
      "totalOrders": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coinGate/latest/actions/list-orders).

## Checkout

Creates a checkout session for an existing CoinGate order.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/checkout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "payCurrency": "string",
  "platformId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coinGate/latest/actions/checkout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "payCurrency": "string",
    "platformId": 1
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
      "doNotConvert": true,
      "id": 1,
      "orderableType": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Checkout action reference](actions/checkout.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/coinGate/latest/actions/checkout).
