# Digistore24: Create Payment Plan

Creates a new payment plan in Digistore24.

```
POST https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-payment-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-payment-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/create-payment-plan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | Product ID |
| `data` | object | yes | Payment plan properties object |
| `data.firstAmount` | number | no | Amount of first payment |
| `data.firstBillingInterval` | string | no | Interval between purchase and second payment |
| `data.currency` | string | no | Three-character currency code |
| `data.otherAmounts` | number | no | Amount for follow-up payments |
| `data.otherBillingIntervals` | string | no | Interval for follow-up payments |
| `data.numberOfInstallments` | number | no | Number of installments |
| `data.isActive` | boolean | no | Whether the payment plan is active |
| `data.cancelPolicy` | string | no | Minimum term policy |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `POST /createPaymentplan` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-plan.md) for the provider-specific parameters and requirements.

