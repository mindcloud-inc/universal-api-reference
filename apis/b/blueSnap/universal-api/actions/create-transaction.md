# BlueSnap: Create Transaction

Creates a transaction in BlueSnap.

```
POST https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/create-transaction', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "cardTransactionType": "string",
      "creditCard": {
        "cardLastFourDigits": "string",
        "cardType": "string"
      },
      "currency": "string",
      "networkTransactionInfo": {
        "networkTransactionId": "string"
      },
      "processingInfo": {
        "processingStatus": "string"
      },
      "softDescriptor": "string",
      "transactionId": "string",
      "usdAmount": 1,
      "vaultedShopperId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Transaction amount. |
| `cardTransactionType` | string | Card transaction type. |
| `creditCard.cardLastFourDigits` | string | Card last four digits. |
| `creditCard.cardType` | string | Card type. |
| `currency` | string | Currency. |
| `networkTransactionInfo.networkTransactionId` | string | Network transaction ID. |
| `processingInfo.processingStatus` | string | Processing status. |
| `softDescriptor` | string | Soft descriptor. |
| `transactionId` | string | Transaction ID. |
| `usdAmount` | number | USD amount. |
| `vaultedShopperId` | number | Vaulted shopper ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `POST /transactions` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

