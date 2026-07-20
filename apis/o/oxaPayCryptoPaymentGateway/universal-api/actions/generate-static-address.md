# OxaPay Crypto Payment Gateway: Generate Static Address

Creates a new static address in OxaPay.

```
POST https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-static-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-static-address" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "network": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-static-address', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "network": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to_currency` | string | no | Optional payout token or currency on the selected network. |
| `network` | string | yes | Blockchain network key. |
| `callback_url` | string | no | Webhook callback URL. |
| `email` | string | no | Customer email. |
| `order_id` | string | no | Merchant order id. |
| `description` | string | no | Static address description. |
| `sandbox` | boolean | no | Create a sandbox static address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": "string",
        "date": 1,
        "memo": "string",
        "network": "string",
        "qrCode": "string",
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
| `data` | object | Generated static-address payload. |
| `data.address` | string | Static deposit address. |
| `data.date` | number | Creation timestamp. |
| `data.memo` | string | Memo or destination tag when provided. |
| `data.network` | string | Selected blockchain network. |
| `data.qrCode` | string | QR code image or data URL. |
| `data.trackId` | number | Static-address track identifier. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `POST /payment/static-address` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-static-address.md) for the provider-specific parameters and requirements.

