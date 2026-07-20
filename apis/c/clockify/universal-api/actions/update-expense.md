# Clockify: Update Expense

Updates an existing expense in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "expenseId": "string",
  "amount": "100",
  "categoryId": "string",
  "changeFields[]": [
    "string"
  ],
  "date": "2026-01-01T00:00:00Z",
  "file": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-expense', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "expenseId": "string",
    "amount": "100",
    "categoryId": "string",
    "changeFields[]": ["string"],
    "date": "2026-01-01T00:00:00Z",
    "file": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `expenseId` | string<string> | yes |  |
| `amount` | number | yes | Example: `100`. |
| `categoryId` | list<string> | yes |  |
| `changeFields[]` | array<string> | yes |  |
| `date` | date | yes | Example: `2026-01-01T00:00:00Z`. |
| `file` | file | yes |  |
| `userId` | list<string> | yes |  |
| `billable` | boolean | no | Example: `true`. |
| `notes` | string | no | Example: `Sample note`. |
| `projectId` | list<string> | no |  |
| `taskId` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": true,
      "categoryId": "string",
      "date": "string",
      "fileId": "string",
      "id": "string",
      "isLocked": true,
      "locked": true,
      "notes": "string",
      "projectId": "string",
      "quantity": 1,
      "taskId": "string",
      "total": 1,
      "userId": "string",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | boolean |  |
| `categoryId` | string |  |
| `date` | string |  |
| `fileId` | string |  |
| `id` | string |  |
| `isLocked` | boolean |  |
| `locked` | boolean |  |
| `notes` | string |  |
| `projectId` | string |  |
| `quantity` | number |  |
| `taskId` | string |  |
| `total` | number |  |
| `userId` | string |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/expenses/:expenseId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-expense.md) for the provider-specific parameters and requirements.

