# Stax: Capture Pre-Auth Transaction

Captures a pre-authorized transaction in Stax.

```
PUT https://connect.mindcloud.co/v1/universal/stax/latest/actions/capture-pre-auth-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stax/latest/actions/capture-pre-auth-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stax/latest/actions/capture-pre-auth-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionid` | string | no | Pre-auth transaction identifier |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "currency": "string",
      "customerId": "string",
      "id": "string",
      "isRefundable": true,
      "isVoidable": true,
      "paymentMethodId": "string",
      "success": true,
      "total": 1,
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `currency` | string | Transaction currency. |
| `customerId` | string | Associated customer identifier. |
| `id` | string | Stax transaction identifier. |
| `isRefundable` | boolean | Whether the transaction can be refunded. |
| `isVoidable` | boolean | Whether the transaction can be voided. |
| `paymentMethodId` | string | Associated payment method identifier. |
| `success` | boolean | Whether the transaction succeeded. |
| `total` | number | Transaction total amount. |
| `type` | string | Transaction type. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `POST /transaction/:transactionid/capture` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-pre-auth-transaction.md) for the provider-specific parameters and requirements.

