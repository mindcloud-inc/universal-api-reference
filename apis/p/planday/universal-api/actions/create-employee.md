# Planday: Create Employee

Creates a new employee in Planday.

```
POST https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "departments[]": [
    1
  ],
  "firstName": "Ava",
  "lastName": "Chen",
  "userName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "departments[]": [1],
    "firstName": "Ava",
    "lastName": "Chen",
    "userName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `departments[]` | array<number> | yes |  |
| `email` | string | no |  |
| `employeeGroups[]` | array<number> | no |  |
| `firstName` | string | yes |  |
| `jobTitle` | string | no |  |
| `lastName` | string | yes |  |
| `primaryDepartmentId` | number | no |  |
| `userName` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateTimeCreated": "2026-05-07T12:00:00.000Z",
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

Through the native Planday API, this operation is `POST /hr/v1.0/employees` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee.md) for the provider-specific parameters and requirements.

