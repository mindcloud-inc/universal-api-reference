# BlueSnap: List Transactions

Retrieves transactions from BlueSnap.

```
GET https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlueSnap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blueSnap/latest/actions/list-transactions?${params}`, {
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
| `pagesize` | string | no | Number of results to return. Default: `10`. |
| `gettotal` | boolean | no | Whether to include total results count. Default: `false`. |
| `merchantTransactionId` | string | no | Filter by merchant transaction ID, if supported. |
| `after` | string | no | Return transactions after this transaction ID. |
| `before` | string | no | Return transactions before this transaction ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lastPage": true,
      "totalResults": 1,
      "transactions": [
        {
          "amount": 1,
          "cardTransactionType": "string",
          "currency": "string",
          "processingInfo": {
            "processingStatus": "string"
          },
          "transactionId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lastPage` | boolean | Whether this is the last page. |
| `totalResults` | number | Total results count. |
| `transactions[].amount` | number | Transaction amount. |
| `transactions[].cardTransactionType` | string | Card transaction type. |
| `transactions[].currency` | string | Currency. |
| `transactions[].processingInfo.processingStatus` | string | Processing status. |
| `transactions[].transactionId` | string | Transaction ID. |

## Native endpoint

Through the native BlueSnap API, this operation is `GET /transactions` (base URL `https://sandbox.bluesnap.com/services/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

