# BlueSnap: Refund Transaction

Creates a refund for a BlueSnap transaction.

```
POST https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/refund-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/refund-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string",
  "amount": "1.00"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/refund-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "string",
    "amount": "1.00"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `transactionId` | string | yes | BlueSnap transaction ID to refund. |
| `amount` | string | yes | Refund amount, e.g. 1.00 Default: `1.00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "refundStatus": "string",
      "refundTransactionId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Refund amount. |
| `refundStatus` | string | Refund processing status. |
| `refundTransactionId` | number | Refund transaction ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `POST /transactions/refund/:transactionId` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-transaction.md) for the provider-specific parameters and requirements.

