# OxaPay Crypto Payment Gateway: Generate White Label

Creates a new white-label payment in OxaPay.

```
POST https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-white-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-white-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "pay_currency": "string",
  "network": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-white-label', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "pay_currency": "string",
    "network": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | White label invoice amount. |
| `pay_currency` | string | yes | Requested crypto payment currency. |
| `network` | string | yes | Blockchain network key. |
| `sandbox` | boolean | no | Create a sandbox white label payment. |
| `order_id` | string | no | Merchant order id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": "string",
        "amount": 1,
        "callbackUrl": "https://example.com",
        "currency": "string",
        "date": 1,
        "description": "string",
        "email": "ava@example.com",
        "expiredAt": 1,
        "feePaidByPayer": 1,
        "lifetime": 1,
        "memo": "string",
        "network": "string",
        "orderId": "string",
        "payAmount": 1,
        "payCurrency": "string",
        "qrCode": "string",
        "rate": 1,
        "trackId": 1,
        "underPaidCoverage": 1
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
| `data` | object | Generated white-label payment payload. |
| `data.address` | string | Deposit address. |
| `data.amount` | number | Requested amount. |
| `data.callbackUrl` | string | Webhook callback URL. |
| `data.currency` | string | Settlement currency. |
| `data.date` | number | Creation timestamp. |
| `data.description` | string | Merchant description. |
| `data.email` | string | Customer email. |
| `data.expiredAt` | number | Invoice expiration time. |
| `data.feePaidByPayer` | number | Fee handling flag. |
| `data.lifetime` | number | Invoice lifetime. |
| `data.memo` | string | Memo or destination tag when provided. |
| `data.network` | string | Blockchain network. |
| `data.orderId` | string | Merchant order identifier. |
| `data.payAmount` | number | Amount the payer must send. |
| `data.payCurrency` | string | Currency used by the payer. |
| `data.qrCode` | string | QR code image or data URL. |
| `data.rate` | number | Exchange rate. |
| `data.trackId` | number | Payment track identifier. |
| `data.underPaidCoverage` | number | Underpayment coverage percentage. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `POST /payment/white-label` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-white-label.md) for the provider-specific parameters and requirements.

