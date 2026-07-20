# Payrexx: List Transactions

Retrieves transactions from Payrexx.

```
GET https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/list-transactions?${params}`, {
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
| `filterDatetimeUtcGreaterThan` | date | no | Lower DateTime limit in the format YYYY-MM-DD HH:MM:SS. Example: `2026-04-01 00:00:00`. |
| `filterDatetimeUtcLessThan` | date | no | Upper DateTime limit in the format YYYY-MM-DD HH:MM:SS. Example: `2026-04-08 23:59:59`. |
| `filterMyTransactionsOnly` | boolean | no | When true, only transactions related to this API key are returned. Example: `false`. |
| `orderByTime` | string | no | ASC or DESC for ordering by time of the transaction. Example: `DESC`. |
| `offset` | number | no | Row count to be used as offset. Example: `0`. |
| `limit` | number | no | Max row count. Example: `10`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `GET Transaction/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

