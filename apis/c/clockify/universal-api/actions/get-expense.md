# Clockify: Get Expense

Retrieves a specific expense from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-expense?connectionId=$CONNECTION_ID&workspaceId=string&expenseId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "expenseId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-expense?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `expenseId` | string<string> | yes |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/expenses/:expenseId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-expense.md) for the provider-specific parameters and requirements.

