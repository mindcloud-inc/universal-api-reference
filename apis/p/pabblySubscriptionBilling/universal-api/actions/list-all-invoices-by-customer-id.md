# Pabbly Subscription Billing: List All Invoices By Customer Id



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-invoices-by-customer-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-invoices-by-customer-id?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-invoices-by-customer-id?${params}`, {
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
| `customerId` | string | no |  |
| `endDate` | string | no |  |
| `queryFilter` | string | no |  |
| `startDate` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customerId": "string",
      "dueAmount": 1,
      "paymentTerm": "string",
      "quantity": 1,
      "status": "string",
      "subscription": {
        "plan": {
          "billingCycle": 1,
          "billingCycleNum": 1,
          "billingPeriod": 1,
          "billingPeriodNum": 1,
          "createdAt": "2026-05-07T12:00:00.000Z",
          "currencyCode": "string",
          "currencySymbol": "string",
          "customPaymentTerm": 1,
          "id": "string",
          "planActive": true,
          "planCode": "string",
          "planDescription": "string",
          "planName": "Ava Chen",
          "planType": "string",
          "price": 1,
          "productId": "string",
          "setupFee": 1,
          "trialPeriod": 1,
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      },
      "subscriptionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customerId` | string |  |
| `dueAmount` | number |  |
| `paymentTerm` | string |  |
| `quantity` | number |  |
| `status` | string |  |
| `subscription.plan.billingCycle` | number |  |
| `subscription.plan.billingCycleNum` | number |  |
| `subscription.plan.billingPeriod` | number |  |
| `subscription.plan.billingPeriodNum` | number |  |
| `subscription.plan.createdAt` | date |  |
| `subscription.plan.currencyCode` | string |  |
| `subscription.plan.currencySymbol` | string |  |
| `subscription.plan.customPaymentTerm` | number |  |
| `subscription.plan.id` | string |  |
| `subscription.plan.planActive` | boolean |  |
| `subscription.plan.planCode` | string |  |
| `subscription.plan.planDescription` | string |  |
| `subscription.plan.planName` | string |  |
| `subscription.plan.planType` | string |  |
| `subscription.plan.price` | number |  |
| `subscription.plan.productId` | string |  |
| `subscription.plan.setupFee` | number |  |
| `subscription.plan.trialPeriod` | number |  |
| `subscription.plan.updatedAt` | date |  |
| `subscriptionId` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/invoices/:customerId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-invoices-by-customer-id.md) for the provider-specific parameters and requirements.

