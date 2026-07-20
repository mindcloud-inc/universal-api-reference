# Hyperzod Universal API Examples

These examples use the MindCloud API key and Hyperzod connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Order Status

Retrieves available order statuses from Hyperzod.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-order-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/list-order-status?${params}`, {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Order Status action reference](actions/list-order-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperzod/latest/actions/list-order-status).

## Bulk Update Product Inventory

Updates product inventory counts in bulk in Hyperzod.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/bulk-update-product-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperzod/latest/actions/bulk-update-product-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Bulk Update Product Inventory action reference](actions/bulk-update-product-inventory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperzod/latest/actions/bulk-update-product-inventory).
