# Harvest: Update Project

Updates an existing project in Harvest.

```
PUT https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | no |  |
| `id` | number | yes |  |
| `name` | string | no |  |
| `code` | string | no |  |
| `isActive` | boolean | no |  |
| `isBillable` | boolean | no |  |
| `isFixedFee` | boolean | no |  |
| `billBy` | string | no |  |
| `hourlyRate` | number | no |  |
| `budgetBy` | string | no |  |
| `budget` | number | no |  |
| `notes` | string | no |  |
| `budgetIsMonthly` | boolean | no |  |
| `costBudget` | number | no |  |
| `costBudgetIncludeExpenses` | boolean | no |  |
| `notifyWhenOverBudget` | boolean | no |  |
| `overBudgetNotificationPercentage` | number | no |  |
| `showBudgetToAll` | boolean | no |  |
| `fee` | number | no |  |
| `startsOn` | string | no |  |
| `endsOn` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billBy": "string",
      "budget": 1,
      "budgetBy": "string",
      "budgetIsMonthly": true,
      "client": {},
      "code": "string",
      "costBudget": 1,
      "costBudgetIncludeExpenses": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endsOn": "2026-05-07T12:00:00.000Z",
      "fee": 1,
      "hourlyRate": 1,
      "id": 1,
      "isActive": true,
      "isBillable": true,
      "isFixedFee": true,
      "name": "Ava Chen",
      "notes": "string",
      "notifyWhenOverBudget": true,
      "overBudgetNotificationDate": "2026-05-07T12:00:00.000Z",
      "overBudgetNotificationPercentage": 1,
      "showBudgetToAll": true,
      "startsOn": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billBy` | string |  |
| `budget` | number |  |
| `budgetBy` | string |  |
| `budgetIsMonthly` | boolean |  |
| `client` | object |  |
| `code` | string |  |
| `costBudget` | number |  |
| `costBudgetIncludeExpenses` | boolean |  |
| `createdAt` | date |  |
| `endsOn` | date |  |
| `fee` | number |  |
| `hourlyRate` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isBillable` | boolean |  |
| `isFixedFee` | boolean |  |
| `name` | string |  |
| `notes` | string |  |
| `notifyWhenOverBudget` | boolean |  |
| `overBudgetNotificationDate` | date |  |
| `overBudgetNotificationPercentage` | number |  |
| `showBudgetToAll` | boolean |  |
| `startsOn` | date |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Harvest API, this operation is `PATCH /v2/projects/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

