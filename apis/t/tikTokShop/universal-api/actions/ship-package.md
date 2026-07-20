# TikTok Shop: Ship Package

Use this API to ship a package. There are two kinds of shipping options available: TikTok Shipping or Seller Shipping.

- TikTok Shipping: Schedule a package handover time for TikTok Shipping carriers to pickup a package from seller.
- Seller Shipping: Seller arranges their own shipping, and uploads a tracking number and shipping_provider_id. Package ID can be obtained from Get Order Detail

```
PUT https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/ship-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/ship-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "package_id": "string",
  "shop_cipher": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/ship-package', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "package_id": "string",
    "shop_cipher": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `package_id` | string | yes |  |
| `pickupSlot.startTime` | number | no | The start date and time of the package pickup time slot. Unix timestamp. |
| `selfShipment.trackingNumber` | string | no | For package with SEND_BY_SELLER as delivery_option (merchant self-shipping mode), you must input a tracking_number to call this API. |
| `handoverMethod` | string | no | Possible values: - PICKUP: A logistics carrier will pick up the package(s) from the seller's pickup address. - DROP_OFF: The seller will need to drop off the package(s) to a designated location. |
| `pickupSlot.endTime` | number | no | The end date and time of the package pickup time slot. Unix timestamp. |
| `selfShipment.shippingProviderid` | string | no | For package with SEND_BY_SELLER as delivery_option (merchant self-shipping mode), you must input a shipping_provider_id to call this API. Please use Get Shipping Providers to obtain the shipping_provider_id. |
| `pickupSlot` | object | no | Pickup time slot. |
| `selfShipment` | object | no | Only needed for merchant self-shipping packages. Check the delivery_option field of Get Package Detail to see how to differentiate platform-logistics and self-shipping. Use the shipping_provider_id retrieved from Get Shipping Providers and upload the corresponding tracking_number. |
| `shop_cipher` | list<string> | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST fulfillment/202309/packages/:package_id/ship` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ship-package.md) for the provider-specific parameters and requirements.

