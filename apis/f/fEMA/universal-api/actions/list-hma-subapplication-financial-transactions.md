# FEMA: List HMA Subapplication Financial Transactions

Retrieves HMA subapplication financial transactions from FEMA.

```
GET https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplication-financial-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FEMA `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplication-financial-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fEMA/latest/actions/list-hma-subapplication-financial-transactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accsLine": "string",
      "amount": 1,
      "commitmentIdentifier": "string",
      "fundCode": "string",
      "id": "string",
      "paymentNumber": "string",
      "subapplicationIdentifier": "string",
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accsLine` | string |  |
| `amount` | number |  |
| `commitmentIdentifier` | string |  |
| `fundCode` | string |  |
| `id` | string |  |
| `paymentNumber` | string |  |
| `subapplicationIdentifier` | string |  |
| `transactionDate` | date |  |
| `transactionType` | string |  |

## Native endpoint

Through the native FEMA API, this operation is `GET /v1/HmaSubapplicationsFinancialTransactions` (base URL `https://www.fema.gov/api/open`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-hma-subapplication-financial-transactions.md) for the provider-specific parameters and requirements.

