# Payhip: Create Coupon

Creates a new coupon in Payhip.

```
POST https://connect.mindcloud.co/v1/universal/payhip/latest/actions/create-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payhip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "couponType": "all_products",
  "code": "SPRING2026"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payhip/latest/actions/create-coupon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "couponType": "all_products",
    "code": "SPRING2026"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `couponType` | list | yes | Choose whether the coupon applies to all products, specific products, or specific collections. One of: `all_products`, `specific_collections`, `specific_products`. Example: `all_products`. |
| `code` | string | yes | The coupon code customers will enter at checkout. Example: `SPRING2026`. |
| `percentOff` | number | no | Percentage discount to apply when using a percentage-based coupon. Example: `20`. |
| `amountOff` | number | no | Fixed amount discount to apply when using an amount-based coupon. Example: `5`. |
| `productKey` | string | no | Required when the coupon targets a specific product. Example: `prod_12345`. |
| `collectionId` | string | no | Required when the coupon targets a specific collection. Example: `collection_12345`. |
| `usageLimit` | number | no | Maximum number of times the coupon can be redeemed. Example: `100`. |
| `minimumPurchaseAmount` | number | no | Minimum purchase amount required before the coupon applies. Example: `25`. |
| `startDate` | string | no | Optional start date for the coupon. Example: `2026-03-12`. |
| `endDate` | string | no | Optional end date for the coupon. Example: `2026-03-31`. |
| `notes` | string | no | Internal notes stored with the coupon. Example: `Spring promotion`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amountOff": 1,
      "code": "string",
      "collectionId": "string",
      "couponType": "string",
      "endDate": "string",
      "id": "string",
      "minimumPurchaseAmount": 1,
      "notes": "string",
      "percentOff": 1,
      "productKey": "string",
      "startDate": "string",
      "usageLimit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountOff` | number | Fixed discount amount when present. |
| `code` | string | Coupon code. |
| `collectionId` | string | Target collection identifier when scoped to a collection. |
| `couponType` | string | The coupon scope type. |
| `endDate` | string | Coupon end date when configured. |
| `id` | string | Payhip coupon identifier. |
| `minimumPurchaseAmount` | number | Minimum purchase threshold when configured. |
| `notes` | string | Internal coupon notes. |
| `percentOff` | number | Percentage discount amount when present. |
| `productKey` | string | Target product key when scoped to a product. |
| `startDate` | string | Coupon start date when configured. |
| `usageLimit` | number | Maximum redemptions when configured. |

## Native endpoint

Through the native Payhip API, this operation is `POST /coupons` (base URL `https://payhip.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon.md) for the provider-specific parameters and requirements.

