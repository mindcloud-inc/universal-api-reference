# EnvelopeBudget: Create Transaction



```
POST https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EnvelopeBudget `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "string",
  "payee": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "string",
    "payee": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budgetId` | string | yes |  |
| `accountId` | string | no |  |
| `envelopeId` | string | no |  |
| `payee` | string | yes | Transaction payee name |
| `date` | string | no |  |
| `amount` | number | no |  |
| `memo` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EnvelopeBudget API returns.

## Native endpoint

Through the native EnvelopeBudget API, this operation is `POST /transactions/:budget_id` (base URL `https://envelopebudget.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

