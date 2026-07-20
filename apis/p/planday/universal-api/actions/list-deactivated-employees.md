# Planday: List Deactivated Employees

Retrieves a list of deactivated employees from Planday.

```
GET https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-deactivated-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-deactivated-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planday/latest/actions/list-deactivated-employees?${params}`, {
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
| `createdFrom` | date | no |  |
| `createdTo` | date | no |  |
| `deactivatedFrom` | date | no |  |
| `deactivatedTo` | date | no |  |
| `limit` | number | no |  |
| `modifiedFrom` | date | no |  |
| `modifiedTo` | date | no |  |
| `offset` | number | no |  |
| `searchQuery` | string | no |  |
| `special[]` | array<string> | no |  |

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
      "id": 1,
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
| `id` | number |  |
| `lastName` | string |  |
| `salaryIdentifier` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native Planday API, this operation is `GET /hr/v1.0/employees/deactivated` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-deactivated-employees.md) for the provider-specific parameters and requirements.

