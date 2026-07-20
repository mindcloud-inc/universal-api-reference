# WebWork Time Tracker: Create Expense

Creates an expense in WebWork Time Tracker.

```
POST https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebWork Time Tracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": 1,
  "expenseName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webWorkTimeTracker/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": 1,
    "expenseName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | number | yes | ID of the workspace. |
| `expenseName` | string | yes | Name of the expense. Required by the provider runtime validation. |
| `amount` | number | no | Expense amount. |
| `categoryId` | string | no | Expense category ID. |
| `description` | string | no | Expense description. |
| `date` | string | no | Expense date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedDte": "string",
      "amount": 1,
      "category": "string",
      "expenseDate": "string",
      "expenseName": "Ava Chen",
      "id": "string",
      "member": "string",
      "note": {},
      "project": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedDte` | string |  |
| `amount` | number |  |
| `category` | string |  |
| `expenseDate` | string |  |
| `expenseName` | string |  |
| `id` | string |  |
| `member` | string |  |
| `note` | object |  |
| `project` | object |  |
| `type` | string |  |

## Native endpoint

Through the native WebWork Time Tracker API, this operation is `POST /expenses` (base URL `https://api.webwork-tracker.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

