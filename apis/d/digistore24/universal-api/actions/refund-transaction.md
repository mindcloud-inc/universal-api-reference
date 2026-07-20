# Digistore24: Refund Transaction

Refunds a payment transaction in Digistore24.

```
PUT https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/refund-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Digistore24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/refund-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/digistore24/latest/actions/refund-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | string | yes | Transaction ID |
| `force` | boolean | no | Force refund |
| `requestDate` | string | no | Refund request date |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Digistore24 API returns.

## Native endpoint

Through the native Digistore24 API, this operation is `POST /refundTransaction` (base URL `https://www.digistore24.com/api/call`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-transaction.md) for the provider-specific parameters and requirements.

