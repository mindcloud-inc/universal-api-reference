# Seven Time: List Users

Retrieves users from a Seven Time workspace.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-users?${params}`, {
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
| `name` | string | no |  |
| `personNumber` | string | no |  |
| `department` | string | no |  |
| `userRole` | string | no |  |
| `isActive` | boolean | no |  |
| `isActivated` | boolean | no |  |
| `defaultSalaryType` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cellPhone": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "employeeNumber": "string",
      "firstName": "Ava",
      "Id": "string",
      "isActivated": true,
      "isActive": true,
      "language": "string",
      "lastName": "Chen",
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "personalNumber": "string",
      "userName": "Ava Chen",
      "userRoleId": 1,
      "workPhone": "string",
      "workSchedules": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cellPhone` | string |  |
| `createdDate` | date |  |
| `email` | string |  |
| `employeeNumber` | string |  |
| `firstName` | string |  |
| `Id` | string |  |
| `isActivated` | boolean |  |
| `isActive` | boolean |  |
| `language` | string |  |
| `lastName` | string |  |
| `modifiedDate` | date |  |
| `personalNumber` | string |  |
| `userName` | string |  |
| `userRoleId` | number |  |
| `workPhone` | string |  |
| `workSchedules` | array<object> |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /users` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

