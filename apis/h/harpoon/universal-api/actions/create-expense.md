# Harpoon: Create Expense

Creates a new expense in Harpoon.

```
POST https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | date | no |  |
| `amount` | number | no |  |
| `vendor` | string | no |  |
| `description` | string | no |  |
| `expenseCategoryId` | number | no |  |
| `projectId` | number | no |  |
| `clientId` | number | no |  |
| `status` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "category": {},
      "category_id": "string",
      "client": {},
      "client_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "date_formatted": "string",
      "description": "string",
      "id": "string",
      "project": {},
      "project_id": "string",
      "receipt_url": "https://example.com",
      "status": "string",
      "taxes": [
        {}
      ],
      "team_id": "string",
      "track_taxes": true,
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `category` | object |  |
| `category_id` | string |  |
| `client` | object |  |
| `client_id` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `date_formatted` | string |  |
| `description` | string |  |
| `id` | string |  |
| `project` | object |  |
| `project_id` | string |  |
| `receipt_url` | string |  |
| `status` | string |  |
| `taxes` | array<object> |  |
| `team_id` | string |  |
| `track_taxes` | boolean |  |
| `vendor` | string |  |

## Native endpoint

Through the native Harpoon API, this operation is `POST /expenses` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

