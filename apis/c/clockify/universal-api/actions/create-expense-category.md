# Clockify: Create Expense Category

Creates a new expense category in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Example Name"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Example Name"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `name` | string | yes | Example: `Example Name`. |
| `hasUnitPrice` | boolean | no | Example: `true`. |
| `priceInCents` | number | no | Example: `100`. |
| `unit` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "hasUnitPrice": true,
      "id": "string",
      "name": "Ava Chen",
      "priceInCents": 1,
      "unit": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `hasUnitPrice` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `priceInCents` | number |  |
| `unit` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/expenses/categories` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense-category.md) for the provider-specific parameters and requirements.

