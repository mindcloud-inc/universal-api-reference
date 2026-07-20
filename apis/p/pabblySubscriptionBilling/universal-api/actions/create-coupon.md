# Pabbly Subscription Billing: Create Coupon



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-coupon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-coupon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-coupon', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `affiliateId` | string | no |  |
| `applyAffiliate` | string | no |  |
| `applyTo` | string | no |  |
| `associatePlans` | string | no |  |
| `couponCode` | string | no |  |
| `couponName` | string | no |  |
| `discount` | string | no |  |
| `discountType` | string | no |  |
| `maximumRedemption` | string | no |  |
| `plansArray` | string | no |  |
| `productId` | string | no |  |
| `redemptionCycle` | string | no |  |
| `redemptionType` | string | no |  |
| `validUpto` | string | no |  |

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
      "discountType": 1,
      "id": "string",
      "maximumRedemption": 1,
      "plansArray": [
        "string"
      ],
      "productId": "string",
      "redemptionCycle": 1,
      "redemptionType": 1,
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
| `discountType` | number |  |
| `id` | string |  |
| `maximumRedemption` | number |  |
| `plansArray[]` | string |  |
| `productId` | string |  |
| `redemptionCycle` | number |  |
| `redemptionType` | number |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `usedRedemption` | number |  |
| `validUpto` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/coupon/:productId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-coupon.md) for the provider-specific parameters and requirements.

