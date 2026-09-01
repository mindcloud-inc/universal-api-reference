# Amark Universal API Examples

These examples use the MindCloud API key and Amark connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Order Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info?connectionId=$CONNECTION_ID&orderNumber=string&orderId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderNumber": "string",
  "orderId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/get-order-info?${params}`, {
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

See the full [Get Order Info action reference](actions/get-order-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amarkAWL/latest/actions/get-order-info).

## Bulk Create Products



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/bulk-create-products" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amarkAWL/latest/actions/bulk-create-products', {
  method: 'POST',
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
      "context": "string",
      "event": "string",
      "status": 1,
      "successData": {
        "description": "string",
        "id": 1,
        "packageUnits": 1,
        "productModifyId": 1,
        "sku": "string",
        "troyOz": 1,
        "type": "string",
        "weightOz": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Products action reference](actions/bulk-create-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/amarkAWL/latest/actions/bulk-create-products).
