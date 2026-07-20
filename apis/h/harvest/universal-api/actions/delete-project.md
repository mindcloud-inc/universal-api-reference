# Harvest: Delete project

Deletes an existing project from Harvest.

```
DELETE https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/delete-project?${params}`, {
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
| `id` | number | yes |  |

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

Through the native Harvest API, this operation is `DELETE /v2/projects/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-project.md) for the provider-specific parameters and requirements.

