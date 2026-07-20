# Harvest: List Projects

Retrieves projects from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-projects?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Harvest API, this operation is `GET /v2/projects` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

