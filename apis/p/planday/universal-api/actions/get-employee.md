# Planday: Get Employee

Retrieves an existing employee from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-employee?connectionId=$CONNECTION_ID&employeeId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/get-employee?${params}`, {
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
| `employeeId` | number | yes |  |
| `special[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cellPhone": "string",
      "cellPhoneCountryCode": "string",
      "cellPhoneCountryPrefix": "string",
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
      "lastName": "Chen",
      "phone": "string",
      "salaryIdentifier": "string",
      "securityGroups": [
        1
      ],
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cellPhone` | string |  |
| `cellPhoneCountryCode` | string |  |
| `cellPhoneCountryPrefix` | string |  |
| `dateTimeCreated` | date |  |
| `departments` | array<number> |  |
| `email` | string |  |
| `employeeGroups` | array<number> |  |
| `employeeTypeId` | number |  |
| `firstName` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `phone` | string |  |
| `salaryIdentifier` | string |  |
| `securityGroups` | array<number> |  |
| `userName` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /hr/v1.0/employees/:employeeId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

