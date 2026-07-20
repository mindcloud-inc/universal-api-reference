# Fiscal Data Service: List Daily Public Debt Transactions

Retrieves daily public debt transactions from Fiscal Data Service.

```
GET https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-public-debt-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiscal Data Service `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-public-debt-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fiscalDataService/latest/actions/list-daily-public-debt-transactions?${params}`, {
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
      "record_date": "2026-05-07T12:00:00.000Z",
      "transaction_mtd_amt": 1,
      "transaction_today_amt": 1,
      "transaction_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `record_date` | date | Record date. |
| `transaction_mtd_amt` | number | Transaction amount month to date. |
| `transaction_today_amt` | number | Transaction amount today. |
| `transaction_type` | string | Transaction type. |

## Native endpoint

Through the native Fiscal Data Service API, this operation is `GET /v1/accounting/dts/public_debt_transactions` (base URL `https://api.fiscaldata.treasury.gov/services/api/fiscal_service`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-daily-public-debt-transactions.md) for the provider-specific parameters and requirements.

