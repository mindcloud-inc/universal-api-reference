# Seven Time: Get User

Retrieves a user from a Seven Time workspace.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | The _id of the user to retrieve. |

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

Through the native Seven Time API, this operation is `GET /users/:_id` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

