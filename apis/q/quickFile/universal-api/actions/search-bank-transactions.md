# QuickFile: Search Bank Transactions



```
GET https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-bank-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QuickFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-bank-transactions?connectionId=$CONNECTION_ID&limit=2&nominalCode=1200&offset=0&sortBy=TransactionDate&sortDirection=DESC" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "limit": "2",
  "nominalCode": "1200",
  "offset": "0",
  "sortBy": "TransactionDate",
  "sortDirection": "DESC"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickFile/latest/actions/search-bank-transactions?${params}`, {
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
| `amountFrom` | number | no | Lower bound for transaction amount |
| `amountTo` | number | no | Upper bound for transaction amount |
| `fromDate` | date | no | Lower bound for transaction date |
| `limit` | number | yes | Maximum number of bank transactions to return Default: `2`. |
| `nominalCode` | number | yes | Nominal code of the bank account to query Default: `1200`. |
| `notes` | string | no | Whole or partial transaction notes |
| `offset` | number | yes | Page offset for bank transaction results Default: `0`. |
| `reference` | string | no | Whole or partial transaction reference |
| `sortBy` | string | yes | Column used to order the transaction results Default: `TransactionDate`. |
| `sortDirection` | string | yes | Direction used to order the transaction results Default: `DESC`. |
| `toDate` | date | no | Upper bound for transaction date |
| `transactionType` | string | no | credits, debits, or omit for both |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "balance": 1,
      "nominalCode": 1,
      "notes": "string",
      "payee": "string",
      "reference": "string",
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionId": 1,
      "transactionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number | Signed transaction amount. |
| `balance` | number | Running balance after the transaction. |
| `nominalCode` | number | Nominal code of the bank ledger queried. |
| `notes` | string | Transaction notes or memo. |
| `payee` | string | Counterparty or payee name. |
| `reference` | string | Bank transaction reference. |
| `transactionDate` | date | Date of the bank transaction. |
| `transactionId` | number | QuickFile transaction identifier. |
| `transactionType` | string | QuickFile transaction type or direction. |

## Native endpoint

Through the native QuickFile API, this operation is `POST /bank/search` (base URL `https://api.quickfile.co.uk/1_2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-bank-transactions.md) for the provider-specific parameters and requirements.

