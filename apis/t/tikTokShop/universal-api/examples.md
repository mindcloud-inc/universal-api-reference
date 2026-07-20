# TikTok Shop Universal API Examples

These examples use the MindCloud API key and TikTok Shop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authorized Shops



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/get-authorized-shops?${params}`, {
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
      "cipher": "string",
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "region": "string",
      "sellerType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Authorized Shops action reference](actions/get-authorized-shops.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tikTokShop/latest/actions/get-authorized-shops).

## Cancel Order

Use this API to cancel an order on behalf of a seller. In the US and UK markets, when an item is out of stock, partial cancellation on the single item level is supported by this API.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/cancel-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "skus.skuId": "string",
  "orderId": "string",
  "skus.quantity": 1,
  "cancelReason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/cancel-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "skus.skuId": "string",
    "orderId": "string",
    "skus.quantity": 1,
    "cancelReason": "string"
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

See the full [Cancel Order action reference](actions/cancel-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tikTokShop/latest/actions/cancel-order).
