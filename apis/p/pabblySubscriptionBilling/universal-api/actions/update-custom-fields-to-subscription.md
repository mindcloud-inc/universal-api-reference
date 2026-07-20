# Pabbly Subscription Billing: Update Custom Fields to Subscription



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-custom-fields-to-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-custom-fields-to-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-custom-fields-to-subscription', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "plan": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currencyCode": "string",
        "currencySymbol": "string",
        "customPaymentTerm": 1,
        "failedPaymentGateway": "string",
        "failedPaymentGatewayArray": [
          "string"
        ],
        "funnel": [
          "string"
        ],
        "id": "string",
        "isMetered": true,
        "metaData": {
          "tasks": "string",
          "workflows": "string"
        },
        "planActive": "string",
        "planCode": "string",
        "planName": "Ava Chen",
        "planType": "string",
        "price": 1,
        "productId": "string",
        "setupFeeType": "string",
        "trialType": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `plan.createdAt` | date |  |
| `plan.currencyCode` | string |  |
| `plan.currencySymbol` | string |  |
| `plan.customPaymentTerm` | number |  |
| `plan.failedPaymentGateway` | string |  |
| `plan.failedPaymentGatewayArray` | array<string> |  |
| `plan.funnel` | array<string> |  |
| `plan.id` | string |  |
| `plan.isMetered` | boolean |  |
| `plan.metaData.tasks` | string |  |
| `plan.metaData.workflows` | string |  |
| `plan.planActive` | string |  |
| `plan.planCode` | string |  |
| `plan.planName` | string |  |
| `plan.planType` | string |  |
| `plan.price` | number |  |
| `plan.productId` | string |  |
| `plan.setupFeeType` | string |  |
| `plan.trialType` | string |  |
| `plan.updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `PUT /v1/subscription/custom-fields/:subscriptionId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-custom-fields-to-subscription.md) for the provider-specific parameters and requirements.

