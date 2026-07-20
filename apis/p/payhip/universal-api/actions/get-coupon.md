# Payhip: Get Coupon

Retrieves a coupon from Payhip by ID.

```
GET https://connect.mindcloud.co/v1/universal/payhip/latest/actions/get-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payhip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payhip/latest/actions/get-coupon?connectionId=$CONNECTION_ID&couponId=1495522137" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "couponId": "1495522137"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payhip/latest/actions/get-coupon?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `couponId` | number | yes | The Payhip coupon ID to retrieve. Example: `1495522137`. |

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

Through the native Payhip API, this operation is `GET /coupons/:coupon_id` (base URL `https://payhip.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-coupon.md) for the provider-specific parameters and requirements.

