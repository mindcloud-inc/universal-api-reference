# Pinch Payments: Create Payment Source

Creates a payment source in Pinch Payments.

```
POST https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-source
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-source" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/create-payment-source', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bankAccountBsb` | string | no | The BSB for the payer's bank account. |
| `bankAccountName` | string | no | The name for the payer's bank account. |
| `bankAccountNumber` | string | no | The bank account number for the payer's bank account. |
| `id` | string | yes | Payer ID in pyr_XXXXXXXXXXXXXX format. |
| `ipAddress` | string | no | The IP address associated with the payment source. |
| `sourceType` | string | no | Currently either bank-account or credit-card. |
| `token` | string | no | The token created by the capture script for the payment source. |

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

Through the native Pinch Payments API, this operation is `POST /payers/[:id]/sources` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-source.md) for the provider-specific parameters and requirements.

