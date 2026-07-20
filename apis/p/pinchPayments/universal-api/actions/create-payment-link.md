# Pinch Payments: Create Payment Link

Creates a payment link in Pinch Payments.

```
POST https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "allowedPaymentMethods[]": [
    "string"
  ],
  "amount": 1,
  "description": "string",
  "payerId": "string",
  "returnUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "allowedPaymentMethods[]": ["string"],
    "amount": 1,
    "description": "string",
    "payerId": "string",
    "returnUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowedPaymentMethods[]` | array<string> | yes |  |
| `amount` | number | yes |  |
| `currency` | string | no |  |
| `description` | string | yes |  |
| `linkExpiryDate` | date | no |  |
| `metadata` | string | no |  |
| `payerId` | string | yes |  |
| `returnUrl` | string | yes |  |
| `surchargePaymentMethods[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `POST /payment-links` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-link.md) for the provider-specific parameters and requirements.

