# EnvelopeBudget: List Transactions



```
GET https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EnvelopeBudget `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0&budgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "budgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/list-transactions?${params}`, {
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
| `budgetId` | string | yes |  |
| `accountId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EnvelopeBudget API returns.

## Native endpoint

Through the native EnvelopeBudget API, this operation is `GET /transactions/:budget_id` (base URL `https://envelopebudget.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

