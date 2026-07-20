# Nexiopay: Refund a transaction



```
POST https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/refund-a-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/refund-a-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/refund-a-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Nexio payment ID to refund. |
| `data` | object | yes | Refund transaction data object documented by Nexio. |

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
| `amount` | number | Refund amount. |
| `currency` | string | Transaction currency. |
| `id` | string | Nexio payment ID. |
| `merchantId` | string | Nexio merchant ID. |
| `message` | string | Nexio response message. |
| `transactionStatus` | string | Refund transaction status. |

## Native endpoint

Through the native Nexiopay API, this operation is `POST /pay/v3/refund` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-a-transaction.md) for the provider-specific parameters and requirements.

