# Goldbelly Universal API Examples

These examples use the MindCloud API key and Goldbelly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-products?${params}`, {
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
      "inventory": 1,
      "name": "Ava Chen",
      "price": 1,
      "sku": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goldbelly/latest/actions/list-products).

## Bulk Update Orders



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orders[]": [
    {}
  ],
  "orders[].customerReferenceNumber": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/bulk-update-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orders[]": [{}],
    "orders[].customerReferenceNumber": 1
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
      "error": {
        "code": 1,
        "message": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Orders action reference](actions/bulk-update-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/goldbelly/latest/actions/bulk-update-orders).
