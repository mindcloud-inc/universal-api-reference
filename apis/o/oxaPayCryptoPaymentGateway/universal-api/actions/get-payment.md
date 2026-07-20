# OxaPay Crypto Payment Gateway: Get Payment

Retrieves a payment from OxaPay.

```
GET https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-payment?connectionId=$CONNECTION_ID&track_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "track_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-payment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `track_id` | string | yes | OxaPay payment track id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "address": "string",
        "amount": 1,
        "currency": "string",
        "date": 1,
        "description": "string",
        "email": "ava@example.com",
        "expiredAt": 1,
        "network": "string",
        "orderId": "string",
        "payAmount": 1,
        "payCurrency": "string",
        "status": "string",
        "trackId": 1,
        "type": "string"
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
| `data` | object | Payment detail response. |
| `data.address` | string | Deposit address. |
| `data.amount` | number | Requested amount. |
| `data.currency` | string | Requested settlement currency. |
| `data.date` | number | Creation timestamp. |
| `data.description` | string | Merchant description. |
| `data.email` | string | Customer email. |
| `data.expiredAt` | number | Invoice expiration time. |
| `data.network` | string | Blockchain network. |
| `data.orderId` | string | Merchant order identifier. |
| `data.payAmount` | number | Amount paid by the payer when available. |
| `data.payCurrency` | string | Currency used by the payer when available. |
| `data.status` | string | Current payment status. |
| `data.trackId` | number | Payment track identifier. |
| `data.type` | string | Payment type. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `GET /payment/:track_id` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payment.md) for the provider-specific parameters and requirements.

