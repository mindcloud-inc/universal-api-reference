# Pabbly Subscription Billing: Get single Plan by Plan ID



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-plan-by-plan-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-plan-by-plan-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-plan-by-plan-id?${params}`, {
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
| `planId` | string | no |  |

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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "currencySymbol": "string",
      "failedPaymentGateway": "string",
      "failedPaymentGatewayArray": [
        "string"
      ],
      "funnel": [
        "string"
      ],
      "funnelCount": "string",
      "gatewaysArray": [
        "string"
      ],
      "id": "string",
      "paymentGateway": "string",
      "planActive": true,
      "planCode": "string",
      "planName": "Ava Chen",
      "planType": "string",
      "price": 1,
      "productId": "string",
      "setupFeeType": 1,
      "specificKeepLive": true,
      "trialAmount": 1,
      "trialType": "string",
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
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `currencySymbol` | string |  |
| `failedPaymentGateway` | string |  |
| `failedPaymentGatewayArray[]` | string |  |
| `funnel[]` | string |  |
| `funnelCount` | string |  |
| `gatewaysArray[]` | string |  |
| `id` | string |  |
| `paymentGateway` | string |  |
| `planActive` | boolean |  |
| `planCode` | string |  |
| `planName` | string |  |
| `planType` | string |  |
| `price` | number |  |
| `productId` | string |  |
| `setupFeeType` | number |  |
| `specificKeepLive` | boolean |  |
| `trialAmount` | number |  |
| `trialType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/plan/:planId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-plan-by-plan-id.md) for the provider-specific parameters and requirements.

