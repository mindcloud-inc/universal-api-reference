# TalentHR: List Employee Managers

Retrieves an employee's managers from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-managers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-managers?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-managers?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "cycleId": 1,
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "effectiveDate": "2026-05-07T12:00:00.000Z",
      "employeeId": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "fromId": 1,
      "id": 1,
      "manager": {},
      "reportsToEmployeeId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `cycleId` | number |  |
| `deletedAt` | date |  |
| `effectiveDate` | date |  |
| `employeeId` | number |  |
| `endDate` | date |  |
| `fromId` | number |  |
| `id` | number |  |
| `manager` | object |  |
| `reportsToEmployeeId` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/managers` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-managers.md) for the provider-specific parameters and requirements.

