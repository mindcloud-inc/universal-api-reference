# Ecwid: Adjust Product Stock

Updates product stock in Ecwid.

```
PUT https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/adjust-product-stock
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ecwid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/adjust-product-stock" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "quantityDelta": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecwid/latest/actions/adjust-product-stock', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "quantityDelta": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | Ecwid product ID. |
| `quantityDelta` | number | yes | Quantity adjustment amount. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ecwid API returns.

## Native endpoint

Through the native Ecwid API, this operation is `PUT /:storeId/products/:productId/inventory` (base URL `https://app.ecwid.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/adjust-product-stock.md) for the provider-specific parameters and requirements.

