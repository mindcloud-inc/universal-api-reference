# aamarPay: Initiate Payment (Form Data)

Creates a payment request in aamarPay using form data.

```
POST https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/initiate-payment-form-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a aamarPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/initiate-payment-form-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "codex-form-20260407-1",
  "successUrl": "https://example.com/success",
  "failUrl": "https://example.com/fail",
  "cancelUrl": "https://example.com/cancel",
  "amount": "10.0",
  "currency": "BDT",
  "description": "Test transaction",
  "customerName": "Codex Test",
  "customerEmail": "test@example.com",
  "customerAddress1": "House 1",
  "customerCity": "Dhaka",
  "customerCountry": "Bangladesh",
  "customerPhone": "+8801704"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/initiate-payment-form-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "codex-form-20260407-1",
    "successUrl": "https://example.com/success",
    "failUrl": "https://example.com/fail",
    "cancelUrl": "https://example.com/cancel",
    "amount": "10.0",
    "currency": "BDT",
    "description": "Test transaction",
    "customerName": "Codex Test",
    "customerEmail": "test@example.com",
    "customerAddress1": "House 1",
    "customerCity": "Dhaka",
    "customerCountry": "Bangladesh",
    "customerPhone": "+8801704"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | string | yes | Unique merchant transaction id for the checkout session. Example: `codex-form-20260407-1`. |
| `successUrl` | string | yes | Redirect URL after a successful payment. Example: `https://example.com/success`. |
| `failUrl` | string | yes | Redirect URL after a failed payment. Example: `https://example.com/fail`. |
| `cancelUrl` | string | yes | Redirect URL after a canceled payment. Example: `https://example.com/cancel`. |
| `amount` | string | yes | Payment amount as a decimal string. Example: `10.0`. |
| `currency` | string | yes | Transaction currency, for example BDT. Default: `BDT`. Example: `BDT`. |
| `description` | string | yes | Merchant-facing description for the transaction. Example: `Test transaction`. |
| `customerName` | string | yes | Customer full name. Example: `Codex Test`. |
| `customerEmail` | string | yes | Customer email address. Example: `test@example.com`. |
| `customerAddress1` | string | yes | Customer primary street address. Example: `House 1`. |
| `customerCity` | string | yes | Customer city. Example: `Dhaka`. |
| `customerCountry` | string | yes | Customer country. Example: `Bangladesh`. |
| `customerPhone` | string | yes | Customer phone number. Example: `+8801704`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "paymentUrl": "https://example.com",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `paymentUrl` | string |  |
| `result` | string |  |

## Native endpoint

Through the native aamarPay API, this operation is `POST /index.php` (base URL `https://sandbox.aamarpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-payment-form-data.md) for the provider-specific parameters and requirements.

