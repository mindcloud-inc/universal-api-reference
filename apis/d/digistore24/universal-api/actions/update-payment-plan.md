# Digistore24: Update Payment Plan

Updates an existing payment plan in Digistore24.

```
PUT https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-payment-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-payment-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentPlanId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/update-payment-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentPlanId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentPlanId` | number | yes | Payment plan ID |
| `firstAmount` | number | no | First payment amount |
| `firstBillingInterval` | string | no | First billing interval |
| `currency` | string | no | Currency code |
| `otherAmounts` | number | no | Subsequent payment amount |
| `otherBillingIntervals` | string | no | Subsequent billing interval |
| `numberOfInstallments` | number | no | Installment count |
| `isActive` | boolean | no | Payment plan active flag |
| `cancelPolicy` | string | no | Cancellation policy |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `PUT /updatePaymentplan` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-payment-plan.md) for the provider-specific parameters and requirements.

