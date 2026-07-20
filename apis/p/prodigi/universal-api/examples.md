# Prodigi Universal API Examples

These examples use the MindCloud API key and Prodigi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Orders

Retrieves a list of orders from Prodigi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/list-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/list-orders?${params}`, {
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
      "charges": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "merchantReference": "string",
      "metadata": {},
      "recipient": {},
      "shipments": [
        {}
      ],
      "shippingMethod": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [List Orders action reference](actions/list-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prodigi/latest/actions/list-orders).

## Cancel Order

Cancels a specific order in Prodigi.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/cancel-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prodigiOrderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/prodigi/latest/actions/cancel-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prodigiOrderId": "string"
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
      "charges": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "items": [
        {}
      ],
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "merchantReference": "string",
      "metadata": {},
      "recipient": {},
      "shipments": [
        {}
      ],
      "shippingMethod": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [Cancel Order action reference](actions/cancel-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/prodigi/latest/actions/cancel-order).
