# Pabbly Subscription Billing: Get Checkout Page By Product Id



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-checkout-page-by-product-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-checkout-page-by-product-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-checkout-page-by-product-id?${params}`, {
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
| `productId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingCycle": 1,
      "billingCycleNum": 1,
      "billingPeriod": 1,
      "billingPeriodNum": 1,
      "checkoutPage": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "planActive": true,
      "planCode": "string",
      "planDescription": "string",
      "planName": "Ava Chen",
      "price": 1,
      "productId": "string",
      "setupFee": 1,
      "trialPeriod": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingCycle` | number |  |
| `billingCycleNum` | number |  |
| `billingPeriod` | number |  |
| `billingPeriodNum` | number |  |
| `checkoutPage` | number |  |
| `createdAt` | date |  |
| `id` | string |  |
| `planActive` | boolean |  |
| `planCode` | string |  |
| `planDescription` | string |  |
| `planName` | string |  |
| `price` | number |  |
| `productId` | string |  |
| `setupFee` | number |  |
| `trialPeriod` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/checkoutpage/:productId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-checkout-page-by-product-id.md) for the provider-specific parameters and requirements.

