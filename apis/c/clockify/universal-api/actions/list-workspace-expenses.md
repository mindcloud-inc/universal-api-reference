# Clockify: List Workspace Expenses

Lists all workspace expenses in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-expenses?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-workspace-expenses?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | list<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyTotals": [
        [
          {}
        ]
      ],
      "expenses": {
        "count": 1,
        "expenses": [
          [
            {}
          ]
        ]
      },
      "weeklyTotals": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyTotals[]` | array<object> |  |
| `dailyTotals[].date` | string |  |
| `dailyTotals[].dateAsInstant` | date |  |
| `dailyTotals[].total` | number |  |
| `expenses` | object |  |
| `expenses.count` | number |  |
| `expenses.expenses[]` | array<object> |  |
| `expenses.expenses[].billable` | boolean |  |
| `expenses.expenses[].category` | object |  |
| `expenses.expenses[].category.archived` | boolean |  |
| `expenses.expenses[].category.hasUnitPrice` | boolean |  |
| `expenses.expenses[].category.id` | string |  |
| `expenses.expenses[].category.name` | string |  |
| `expenses.expenses[].category.priceInCents` | number |  |
| `expenses.expenses[].category.unit` | string |  |
| `expenses.expenses[].category.workspaceId` | string |  |
| `expenses.expenses[].date` | string |  |
| `expenses.expenses[].fileId` | string |  |
| `expenses.expenses[].fileName` | string |  |
| `expenses.expenses[].id` | string |  |
| `expenses.expenses[].isLocked` | boolean |  |
| `expenses.expenses[].locked` | boolean |  |
| `expenses.expenses[].notes` | string |  |
| `expenses.expenses[].project` | object |  |
| `expenses.expenses[].project.clientId` | string |  |
| `expenses.expenses[].project.clientName` | string |  |
| `expenses.expenses[].project.color` | string |  |
| `expenses.expenses[].project.id` | string |  |
| `expenses.expenses[].project.name` | string |  |
| `expenses.expenses[].quantity` | number |  |
| `expenses.expenses[].task` | object |  |
| `expenses.expenses[].task.id` | string |  |
| `expenses.expenses[].task.name` | string |  |
| `expenses.expenses[].total` | number |  |
| `expenses.expenses[].userId` | string |  |
| `expenses.expenses[].workspaceId` | string |  |
| `weeklyTotals[]` | array<object> |  |
| `weeklyTotals[].date` | string |  |
| `weeklyTotals[].total` | number |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/expenses` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-workspace-expenses.md) for the provider-specific parameters and requirements.

