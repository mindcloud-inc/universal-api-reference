# OxaPay Crypto Payment Gateway: Generate Invoice

Creates a new invoice in OxaPay.

```
POST https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Invoice amount. |
| `currency` | string | yes | Fiat currency symbol. |
| `sandbox` | boolean | no | Create a sandbox invoice. |
| `order_id` | string | no | Merchant order id. |
| `description` | string | no | Invoice description. |
| `pay_currency` | string | no | Requested crypto payment currency. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "date": 1,
        "expiredAt": 1,
        "paymentUrl": "https://example.com",
        "trackId": 1
      },
      "error": {},
      "message": "string",
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Generated invoice payload. |
| `data.date` | number | Creation timestamp. |
| `data.expiredAt` | number | Invoice expiration time. |
| `data.paymentUrl` | string | Hosted payment URL. |
| `data.trackId` | number | Payment track identifier. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `POST /payment/invoice` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-invoice.md) for the provider-specific parameters and requirements.

