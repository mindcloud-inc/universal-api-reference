# EnvelopeBudget: Update Category



```
PUT https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EnvelopeBudget `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "budgetId": "string",
  "categoryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/envelopeBudget/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "budgetId": "string",
    "categoryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `budgetId` | string | yes |  |
| `categoryId` | string | yes |  |
| `name` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EnvelopeBudget API returns.

## Native endpoint

Through the native EnvelopeBudget API, this operation is `PATCH /categories/:budget_id/:category_id` (base URL `https://envelopebudget.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

