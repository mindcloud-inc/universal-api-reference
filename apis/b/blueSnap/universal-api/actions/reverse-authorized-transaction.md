# BlueSnap: Reverse Authorized Transaction

Reverses an authorized BlueSnap transaction.

```
PUT https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/reverse-authorized-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/reverse-authorized-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/reverse-authorized-transaction', {
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
| `transactionId` | string | yes | Authorized transaction ID to reverse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cardTransactionType": "string",
      "currency": "string",
      "openToCapture": 1,
      "processingInfo": {
        "processingStatus": "string"
      },
      "transactionId": "string",
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Authorized amount. |
| `cardTransactionType` | string | Card transaction type. |
| `currency` | string | Currency. |
| `openToCapture` | number | Remaining open-to-capture amount. |
| `processingInfo.processingStatus` | string | Processing status. |
| `transactionId` | string | Transaction ID. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `PUT /transactions` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-authorized-transaction.md) for the provider-specific parameters and requirements.

