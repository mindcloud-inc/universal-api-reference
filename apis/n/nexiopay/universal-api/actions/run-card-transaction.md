# Nexiopay: Run card transaction



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-card-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-card-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "processingOptions": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/run-card-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "processingOptions": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Card transaction and customer data object documented by Nexio. |
| `processingOptions` | object | yes | Processing options object documented by Nexio. |
| `card` | object | no | Card information object documented by Nexio. |
| `tokenex` | object | no | TokenEx payment token object documented by Nexio. |
| `recurringId` | string | no | Recurring payment token or recurring ID documented by Nexio. |
| `terminal` | object | no | Terminal transaction object documented by Nexio. |
| `clientIp` | string | no | Client IP address for the request. |
| `isAuthOnly` | boolean | no | Whether to run an auth-only transaction. |
| `paymentMethod` | string | no | Payment method selector documented by Nexio. |
| `external3ds` | object | no | External 3DS data object documented by Nexio. |
| `installment` | object | no | Installment data object documented by Nexio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "merchantId": "string",
      "message": "string",
      "transactionStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `currency` | string | Transaction currency. |
| `id` | string | Nexio payment ID. |
| `merchantId` | string | Nexio merchant ID. |
| `message` | string | Nexio response message. |
| `transactionStatus` | string | Transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/process` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-card-transaction.md) for the provider-specific parameters and requirements.

