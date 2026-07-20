# TikTok Shop: Mark Package As Shipped

This API is currently exclusive to the following markets: US, UK, ES, IE.

This API is for sellers who fulfill orders through their own selected/preferred logistics carrier, and allows sellers to upload valid package information (items in packages, shipping provider information, and tracking number) orders/order line items to TikTok Shop. Use Get Shipping Providers API to retrieve the shipping_provider_id for shipping providers.

```
POST https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/mark-package-as-shipped
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/mark-package-as-shipped" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "order_id": "string",
  "shipping_provider_id": "string",
  "shop_cipher": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/mark-package-as-shipped', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "order_id": "string",
    "shipping_provider_id": "string",
    "shop_cipher": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order_id` | string | yes |  |
| `shipping_provider_id` | string | yes |  |
| `shop_cipher` | list<string> | yes |  |
| `tracking_number` | string | no |  |
| `order_line_item_ids[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST fulfillment/202309/orders/:order_id/packages` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/mark-package-as-shipped.md) for the provider-specific parameters and requirements.

