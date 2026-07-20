# Pabbly Subscription Billing: List All Subscriptions



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-subscriptions?${params}`, {
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
| `billingCycle` | string | no | Supported value: onetime,lifetime,specific |
| `billingPeriod` | string | no | Supported value: w,m,y |
| `planId` | string | no | Uniquely identifies the plan. |
| `productId` | string | no | Uniquely identifies the product. |
| `status` | string | no | Supported subscription status such as live, pending, cancelled, expired, dunning, trial, nonrenewing, unpaid, or paused. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addons": [
        {
          "adjustedAmount": 1,
          "associatePlans": "string",
          "billingCycle": 1,
          "billingPeriod": 1,
          "categoryArray": [
            "string"
          ],
          "code": "string",
          "id": "string",
          "name": "Ava Chen",
          "plansArray": "string",
          "price": 1,
          "productId": "string",
          "quantity": 1,
          "userId": "string"
        }
      ],
      "currencySymbol": "string",
      "gatewayType": "string",
      "paymentMethod": "string",
      "paymentTerms": "string",
      "plan": {
        "billingCycle": 1,
        "billingCycleNum": 1,
        "billingPeriod": 1,
        "billingPeriodNum": 1,
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
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": "string"
      },
      "setupFee": 1,
      "taxable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addons[].adjustedAmount` | number |  |
| `addons[].associatePlans` | string |  |
| `addons[].billingCycle` | number |  |
| `addons[].billingPeriod` | number |  |
| `addons[].categoryArray[]` | string |  |
| `addons[].code` | string |  |
| `addons[].id` | string |  |
| `addons[].name` | string |  |
| `addons[].plansArray` | string |  |
| `addons[].price` | number |  |
| `addons[].productId` | string |  |
| `addons[].quantity` | number |  |
| `addons[].userId` | string |  |
| `currencySymbol` | string |  |
| `gatewayType` | string |  |
| `paymentMethod` | string |  |
| `paymentTerms` | string |  |
| `plan.billingCycle` | number |  |
| `plan.billingCycleNum` | number |  |
| `plan.billingPeriod` | number |  |
| `plan.billingPeriodNum` | number |  |
| `plan.createdAt` | date |  |
| `plan.id` | string |  |
| `plan.planActive` | boolean |  |
| `plan.planCode` | string |  |
| `plan.planDescription` | string |  |
| `plan.planName` | string |  |
| `plan.price` | number |  |
| `plan.productId` | string |  |
| `plan.setupFee` | number |  |
| `plan.trialPeriod` | number |  |
| `plan.updatedAt` | date |  |
| `plan.userId` | string |  |
| `setupFee` | number |  |
| `taxable` | boolean |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/subscriptions` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-subscriptions.md) for the provider-specific parameters and requirements.

