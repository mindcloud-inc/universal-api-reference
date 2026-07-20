# iPaymu: Create Direct Payment

Create a direct payment and return the payment details for the selected channel.

```
POST https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-direct-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-direct-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "phone": "string",
  "email": "ava@example.com",
  "amount": 1,
  "notifyUrl": "https://example.com",
  "referenceId": "string",
  "paymentMethod": "string",
  "paymentChannel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/create-direct-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "phone": "string",
    "email": "ava@example.com",
    "amount": 1,
    "notifyUrl": "https://example.com",
    "referenceId": "string",
    "paymentMethod": "string",
    "paymentChannel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Customer name. |
| `phone` | string | yes | Customer phone number. |
| `email` | string | yes | Customer email address. |
| `amount` | number | yes | Payment amount. |
| `notifyUrl` | string | yes | Callback URL for payment updates. |
| `referenceId` | string | yes | Merchant reference for the payment. |
| `paymentMethod` | string | yes | Payment method code, for example va. |
| `paymentChannel` | string | yes | Payment channel code, for example bca. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "escrow": true,
      "expired": "string",
      "fee": 1,
      "feeDirection": "string",
      "paymentName": "Ava Chen",
      "paymentNo": "string",
      "referenceId": "string",
      "sessionId": "string",
      "subTotal": 1,
      "total": 1,
      "transactionId": 1,
      "via": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `escrow` | boolean |  |
| `expired` | string |  |
| `fee` | number |  |
| `feeDirection` | string |  |
| `paymentName` | string |  |
| `paymentNo` | string |  |
| `referenceId` | string |  |
| `sessionId` | string |  |
| `subTotal` | number |  |
| `total` | number |  |
| `transactionId` | number |  |
| `via` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /payment/direct` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-direct-payment.md) for the provider-specific parameters and requirements.

