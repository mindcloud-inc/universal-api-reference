# Pabbly Subscription Billing: Delete Coupon



```
DELETE https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-coupon?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/delete-coupon?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "applyTo": "string",
      "associatePlans": "string",
      "couponCode": "string",
      "couponName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discount": 1,
      "discountType": "string",
      "id": "string",
      "maximumRedemption": 1,
      "plansArray": [
        "string"
      ],
      "productId": "string",
      "redemptionCycle": 1,
      "redemptionType": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usedRedemption": 1,
      "validUpto": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applyTo` | string |  |
| `associatePlans` | string |  |
| `couponCode` | string |  |
| `couponName` | string |  |
| `createdAt` | date |  |
| `discount` | number |  |
| `discountType` | string |  |
| `id` | string |  |
| `maximumRedemption` | number |  |
| `plansArray` | array<string> |  |
| `productId` | string |  |
| `redemptionCycle` | number |  |
| `redemptionType` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `usedRedemption` | number |  |
| `validUpto` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `DELETE /v1/coupons/:couponId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-coupon.md) for the provider-specific parameters and requirements.

