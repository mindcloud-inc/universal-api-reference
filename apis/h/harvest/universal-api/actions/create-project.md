# Harvest: Create Project

Creates a new project in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": 1,
  "name": "Ava Chen",
  "isBillable": true,
  "billBy": "string",
  "budgetBy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": 1,
    "name": "Ava Chen",
    "isBillable": true,
    "billBy": "string",
    "budgetBy": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | number | yes |  |
| `name` | string | yes |  |
| `code` | string | no |  |
| `isActive` | boolean | no |  |
| `isBillable` | boolean | yes |  |
| `isFixedFee` | boolean | no |  |
| `billBy` | string | yes |  |
| `hourlyRate` | number | no |  |
| `budgetBy` | string | yes |  |
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

Through the native Harvest API, this operation is `POST /v2/projects` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

