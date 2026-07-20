# Megaventory Universal API Examples

These examples use the MindCloud API key and Megaventory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves existing product records from Megaventory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/list-products?${params}`, {
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
      "mvProducts": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/megaventory/latest/actions/list-products).

## Bulk Update Purchase Orders

Updates purchase orders in Megaventory in bulk.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-purchase-orders" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "PurchaseOrders": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/megaventory/latest/actions/bulk-update-purchase-orders', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "PurchaseOrders": {}
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
      "PurchaseOrdersResponses": [
        {}
      ],
      "ResponseStatus": {}
    }
  ],
  "meta": {}
}
```

See the full [Bulk Update Purchase Orders action reference](actions/bulk-update-purchase-orders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/megaventory/latest/actions/bulk-update-purchase-orders).
