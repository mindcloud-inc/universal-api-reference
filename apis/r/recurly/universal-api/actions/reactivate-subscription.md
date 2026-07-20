# Recurly: Reactivate Subscription



```
PUT https://connect.mindcloud.co/v1/universal/recurly/latest/actions/reactivate-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/reactivate-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurly/latest/actions/reactivate-subscription', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "actionResult": {},
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "activeInvoiceId": "string",
      "addOns": [
        {}
      ],
      "addOnsTotal": 1,
      "autoRenew": true,
      "billingInfoId": "string",
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "collectionMethod": "string",
      "convertedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditApplicationPolicy": {},
      "currency": "string",
      "currentPeriodEndsAt": "2026-05-07T12:00:00.000Z",
      "currentPeriodStartedAt": "2026-05-07T12:00:00.000Z",
      "currentTermEndsAt": "2026-05-07T12:00:00.000Z",
      "currentTermStartedAt": "2026-05-07T12:00:00.000Z",
      "customerNotes": "string",
      "customFields": [
        {}
      ],
      "expirationReason": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "gatewayCode": "string",
      "id": "string",
      "netTerms": 1,
      "netTermsType": "string",
      "nextAction": {},
      "object": "string",
      "pausedAt": "2026-05-07T12:00:00.000Z",
      "plan": {},
      "poNumber": "string",
      "priceSegmentId": "string",
      "quantity": 1,
      "rampIntervals": [
        {}
      ],
      "remainingBillingCycles": 1,
      "remainingPauseCycles": 1,
      "renewalBillingCycles": 1,
      "shipping": {},
      "startedWithGift": true,
      "state": "string",
      "subtotal": 1,
      "tax": 1,
      "taxInfo": {},
      "termsAndConditions": "string",
      "total": 1,
      "totalBillingCycles": 1,
      "trialEndsAt": "2026-05-07T12:00:00.000Z",
      "trialStartedAt": "2026-05-07T12:00:00.000Z",
      "unitAmount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `actionResult` | object |  |
| `activatedAt` | date |  |
| `activeInvoiceId` | string |  |
| `addOns` | array<object> |  |
| `addOnsTotal` | number |  |
| `autoRenew` | boolean |  |
| `billingInfoId` | string |  |
| `canceledAt` | date |  |
| `collectionMethod` | string |  |
| `convertedAt` | date |  |
| `createdAt` | date |  |
| `creditApplicationPolicy` | object |  |
| `currency` | string |  |
| `currentPeriodEndsAt` | date |  |
| `currentPeriodStartedAt` | date |  |
| `currentTermEndsAt` | date |  |
| `currentTermStartedAt` | date |  |
| `customerNotes` | string |  |
| `customFields` | array<object> |  |
| `expirationReason` | string |  |
| `expiresAt` | date |  |
| `gatewayCode` | string |  |
| `id` | string |  |
| `netTerms` | number |  |
| `netTermsType` | string |  |
| `nextAction` | object |  |
| `object` | string |  |
| `pausedAt` | date |  |
| `plan` | object |  |
| `poNumber` | string |  |
| `priceSegmentId` | string |  |
| `quantity` | number |  |
| `rampIntervals` | array<object> |  |
| `remainingBillingCycles` | number |  |
| `remainingPauseCycles` | number |  |
| `renewalBillingCycles` | number |  |
| `shipping` | object |  |
| `startedWithGift` | boolean |  |
| `state` | string |  |
| `subtotal` | number |  |
| `tax` | number |  |
| `taxInfo` | object |  |
| `termsAndConditions` | string |  |
| `total` | number |  |
| `totalBillingCycles` | number |  |
| `trialEndsAt` | date |  |
| `trialStartedAt` | date |  |
| `unitAmount` | number |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Recurly API, this operation is `PUT /subscriptions/:subscription_id/reactivate` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reactivate-subscription.md) for the provider-specific parameters and requirements.

