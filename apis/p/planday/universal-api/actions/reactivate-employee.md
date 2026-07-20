# Planday: Reactivate Employee

Reactivates a deactivated employee in Planday.

```
PUT https://connect.mindcloud.co/v1/universal/planday/latest/actions/reactivate-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planday/latest/actions/reactivate-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/reactivate-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no |  |
| `departments[]` | array<number> | no |  |
| `employeeId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateTimeCreated": "2026-05-07T12:00:00.000Z",
      "dateTimeModified": "2026-05-07T12:00:00.000Z",
      "departments": [
        1
      ],
      "email": "ava@example.com",
      "employeeGroups": [
        1
      ],
      "employeeTypeId": 1,
      "firstName": "Ava",
      "gender": "string",
      "id": 1,
      "jobTitle": "string",
      "lastName": "Chen",
      "salaryIdentifier": "string",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateTimeCreated` | date |  |
| `dateTimeModified` | date |  |
| `departments` | array<number> |  |
| `email` | string |  |
| `employeeGroups` | array<number> |  |
| `employeeTypeId` | number |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `salaryIdentifier` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Planday API, this operation is `PUT /hr/v1.0/employees/reactivate/:employeeId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reactivate-employee.md) for the provider-specific parameters and requirements.

