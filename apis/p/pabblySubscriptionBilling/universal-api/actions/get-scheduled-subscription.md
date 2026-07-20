# Pabbly Subscription Billing: Get Scheduled Subscription



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-scheduled-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-scheduled-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-scheduled-subscription?${params}`, {
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
| `subscriptionId` | string | no | Pabbly Subscription ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "newPlan": {
        "billingCycle": 1,
        "billingCycleNum": 1,
        "billingPeriod": 1,
        "billingPeriodNum": 1,
        "bumpOffer": {
          "description": "string",
          "planId": "string",
          "tagLine": "string",
          "titleLabel": "string"
        },
        "createdAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "planActive": true,
        "planCode": "string",
        "planDescription": "string",
        "planName": "Ava Chen",
        "price": 1,
        "productId": "string",
        "redirectUrl": "https://example.com",
        "setupFee": 1,
        "trialPeriod": 1,
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "oldPlan": {
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
| `newPlan.billingCycle` | number |  |
| `newPlan.billingCycleNum` | number |  |
| `newPlan.billingPeriod` | number |  |
| `newPlan.billingPeriodNum` | number |  |
| `newPlan.bumpOffer.description` | string |  |
| `newPlan.bumpOffer.planId` | string |  |
| `newPlan.bumpOffer.tagLine` | string |  |
| `newPlan.bumpOffer.titleLabel` | string |  |
| `newPlan.createdAt` | date |  |
| `newPlan.id` | string |  |
| `newPlan.planActive` | boolean |  |
| `newPlan.planCode` | string |  |
| `newPlan.planDescription` | string |  |
| `newPlan.planName` | string |  |
| `newPlan.price` | number |  |
| `newPlan.productId` | string |  |
| `newPlan.redirectUrl` | string |  |
| `newPlan.setupFee` | number |  |
| `newPlan.trialPeriod` | number |  |
| `newPlan.updatedAt` | date |  |
| `oldPlan.billingCycle` | number |  |
| `oldPlan.billingCycleNum` | number |  |
| `oldPlan.billingPeriod` | number |  |
| `oldPlan.billingPeriodNum` | number |  |
| `oldPlan.createdAt` | date |  |
| `oldPlan.id` | string |  |
| `oldPlan.planActive` | boolean |  |
| `oldPlan.planCode` | string |  |
| `oldPlan.planDescription` | string |  |
| `oldPlan.planName` | string |  |
| `oldPlan.price` | number |  |
| `oldPlan.productId` | string |  |
| `oldPlan.setupFee` | number |  |
| `oldPlan.trialPeriod` | number |  |
| `oldPlan.updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/scheduledchanges/:subscriptionId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-scheduled-subscription.md) for the provider-specific parameters and requirements.

