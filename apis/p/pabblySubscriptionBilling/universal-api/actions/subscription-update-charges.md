# Pabbly Subscription Billing: Subscription Update Charges



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/subscription-update-charges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/subscription-update-charges" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/subscription-update-charges', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addons` | string | no |  |
| `couponCode` | string | no |  |
| `planId` | string | no |  |
| `price` | string | no |  |
| `quantity` | string | no |  |
| `setupFee` | string | no |  |
| `subscriptionId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chargeAmount": 1,
      "creditApplied": [
        "string"
      ],
      "currentPlanName": "Ava Chen",
      "currentPlanPrice": 1,
      "currentPlanQuantity": 1,
      "currentPlanTotal": 1,
      "newCredits": 1,
      "newPlanName": "Ava Chen",
      "newPlanPrice": 1,
      "newPlanQuantity": 1,
      "newPlanTotal": "string",
      "remainingDays": 1,
      "totalCreditAmount": 1,
      "totalTax": "string",
      "transactionNote": "string",
      "updateType": "2026-05-07T12:00:00.000Z",
      "usedAmount": 1,
      "usedDays": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chargeAmount` | number |  |
| `creditApplied[]` | string |  |
| `currentPlanName` | string |  |
| `currentPlanPrice` | number |  |
| `currentPlanQuantity` | number |  |
| `currentPlanTotal` | number |  |
| `newCredits` | number |  |
| `newPlanName` | string |  |
| `newPlanPrice` | number |  |
| `newPlanQuantity` | number |  |
| `newPlanTotal` | string |  |
| `remainingDays` | number |  |
| `totalCreditAmount` | number |  |
| `totalTax` | string |  |
| `transactionNote` | string |  |
| `updateType` | date |  |
| `usedAmount` | number |  |
| `usedDays` | number |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/subscription/:subscriptionId/update_charges` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/subscription-update-charges.md) for the provider-specific parameters and requirements.

