# TalentHR: List Employee Time Off Budgets

Retrieves an employee's time off budgets from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-budgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-budgets?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-time-off-budgets?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "budget": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "employeeId": 1,
      "id": 1,
      "originalBudget": "string",
      "paid": true,
      "timeOffCycleId": 1,
      "timeoffTypeId": 1,
      "timeoffTypeName": "Ava Chen",
      "timeoffTypeSlug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "usedBudget": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budget` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `employeeId` | number |  |
| `id` | number |  |
| `originalBudget` | string |  |
| `paid` | boolean |  |
| `timeOffCycleId` | number |  |
| `timeoffTypeId` | number |  |
| `timeoffTypeName` | string |  |
| `timeoffTypeSlug` | string |  |
| `updatedAt` | date |  |
| `usedBudget` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/time-off-budgets` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-time-off-budgets.md) for the provider-specific parameters and requirements.

