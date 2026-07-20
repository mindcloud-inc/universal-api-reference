# Pabbly Subscription Billing: Update Plan



```
PUT https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/update-plan', {
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
| `billingCycle` | string | no |  |
| `billingCycleNum` | string | no |  |
| `billingPeriod` | string | no |  |
| `billingPeriodNum` | string | no |  |
| `currencyCode` | string | no |  |
| `failedPaymentGateway` | string | no |  |
| `failedPaymentGatewayArray` | string | no |  |
| `gatewaysArray` | string | no |  |
| `metaData` | string | no |  |
| `paymentGateway` | string | no |  |
| `paymentTerm` | string | no |  |
| `planActive` | string | no |  |
| `planCode` | string | no |  |
| `planDescription` | string | no |  |
| `planId` | string | no |  |
| `planName` | string | no |  |
| `planType` | string | no |  |
| `price` | string | no |  |
| `productId` | string | no |  |
| `redirectUrl` | string | no |  |
| `setupFee` | string | no |  |
| `specificKeepLive` | string | no |  |
| `trialAmount` | string | no |  |
| `trialPeriod` | string | no |  |
| `trialType` | string | no |  |
| `variableIncreasePrice` | string | no |  |
| `variableMaxPriceAmount` | string | no |  |
| `variablePeriodNum` | string | no |  |
| `variableStartTime` | string | no |  |
| `variableType` | string | no |  |

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
      "redirectUrl": "https://example.com",
      "setupFeeType": 1,
      "tiers": [
        {
          "endingUnit": "string",
          "price": 1,
          "startingUnit": "string"
        }
      ],
      "trialAmount": 1,
      "trialPeriod": 1,
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
| `gatewaysArray[]` | string |  |
| `id` | string |  |
| `paymentGateway` | string |  |
| `planActive` | boolean |  |
| `planCode` | string |  |
| `planName` | string |  |
| `planType` | string |  |
| `price` | number |  |
| `productId` | string |  |
| `redirectUrl` | string |  |
| `setupFeeType` | number |  |
| `tiers[].endingUnit` | string |  |
| `tiers[].price` | number |  |
| `tiers[].startingUnit` | string |  |
| `trialAmount` | number |  |
| `trialPeriod` | number |  |
| `trialType` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `PUT /v1/plan/update/:planId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-plan.md) for the provider-specific parameters and requirements.

