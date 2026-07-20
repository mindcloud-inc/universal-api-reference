# TikTok Shop: Create Packages



```
POST https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-packages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-packages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/create-packages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `weight.unit` | list | no | Available values: - GRAM - POUND |
| `dimension.length` | string | no |  |
| `orderId` | string | yes |  |
| `weight.value` | string | no |  |
| `dimension.width` | string | no |  |
| `dimension.height` | string | no |  |
| `dimension.unit` | list | no | The unit of measurement for the package dimensions. Available values: - CM - INCH |
| `shopCipher` | list<string> | no |  |
| `dimension` | object | no |  |
| `order_line_item_ids` | string | no |  |
| `shippingServiceId` | string | no |  |
| `weight` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST fulfillment/202309/packages` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-packages.md) for the provider-specific parameters and requirements.

