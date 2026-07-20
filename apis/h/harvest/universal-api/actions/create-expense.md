# Harvest: Create Expense

Creates a new expense in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-expense
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-expense" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "expenseCategoryId": 1,
  "spentDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-expense', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "expenseCategoryId": 1,
    "spentDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `expenseCategoryId` | number | yes |  |
| `spentDate` | string | yes |  |
| `units` | number | no |  |
| `totalCost` | number | no |  |
| `notes` | string | no |  |
| `billable` | boolean | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "billable": true,
      "client": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expenseCategory": {},
      "id": 1,
      "invoice": {},
      "isBilled": true,
      "isClosed": true,
      "isLocked": true,
      "lockedReason": "string",
      "notes": "string",
      "project": {},
      "receipt": {},
      "spentDate": "2026-05-07T12:00:00.000Z",
      "totalCost": 1,
      "units": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "userAssignment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `billable` | boolean |  |
| `client` | object |  |
| `createdAt` | date |  |
| `expenseCategory` | object |  |
| `id` | number |  |
| `invoice` | object |  |
| `isBilled` | boolean |  |
| `isClosed` | boolean |  |
| `isLocked` | boolean |  |
| `lockedReason` | string |  |
| `notes` | string |  |
| `project` | object |  |
| `receipt` | object |  |
| `spentDate` | date |  |
| `totalCost` | number |  |
| `units` | number |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `userAssignment` | object |  |

## Native endpoint

Through the native Harvest API, this operation is `POST /v2/expenses` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expense.md) for the provider-specific parameters and requirements.

