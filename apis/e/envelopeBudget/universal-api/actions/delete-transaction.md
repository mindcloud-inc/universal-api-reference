# EnvelopeBudget: Delete Transaction



```
DELETE https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/delete-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EnvelopeBudget `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/delete-transaction?connectionId=$CONNECTION_ID&budgetId=string&transactionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "budgetId": "string",
  "transactionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/delete-transaction?${params}`, {
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
| `transactionId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EnvelopeBudget API returns.

## Native endpoint

Through the native EnvelopeBudget API, this operation is `DELETE /transactions/:budget_id/:transaction_id` (base URL `https://envelopebudget.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-transaction.md) for the provider-specific parameters and requirements.

