# TikTok Shop: Update Inventory



```
PUT https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/update-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/update-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/update-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product_id` | string | yes |  |
| `skus[].id` | string | no |  |
| `skus[].inventory[].warehouseId` | string | no |  |
| `skus[].inventory[]` | array | no |  |
| `skus[].inventory[].availableStock` | number | no |  |
| `shopCipher` | list<string> | no |  |
| `skus[]` | array | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST product/202309/products/:product_id/inventory/update` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory.md) for the provider-specific parameters and requirements.

