# Clockify: Create Expense

Creates a new expense in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "amount": "100",
  "categoryId": "string",
  "date": "2026-01-01T00:00:00Z",
  "file": "string",
  "projectId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "amount": "100",
    "categoryId": "string",
    "date": "2026-01-01T00:00:00Z",
    "file": "string",
    "projectId": "string",
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
| `amount` | number | yes | Example: `100`. |
| `categoryId` | list<string> | yes |  |
| `date` | date | yes | Example: `2026-01-01T00:00:00Z`. |
| `file` | file | yes |  |
| `projectId` | list<string> | yes |  |
| `userId` | list<string> | yes |  |
| `billable` | boolean | no | Example: `true`. |
| `notes` | string | no | Example: `Sample note`. |
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

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/expenses` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

