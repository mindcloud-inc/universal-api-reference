# actiTIME: List Users

Retrieves a list of users from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users?${params}`, {
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
| `active` | boolean | no | Filter active vs inactive users. |
| `department` | string | no |  |
| `email` | string | no |  |
| `ids` | string | no |  |
| `includeReferenced` | string | no |  |
| `name` | string | no |  |
| `sort` | string | no | Sorting tokens like +lastName or -hired. |
| `timeZoneGroup` | string | no |  |
| `username` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "allowedActions": {
        "canSubmitTimetrack": true
      },
      "departmentId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "hired": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "lastName": "Chen",
      "middleName": "Ava Chen",
      "releaseDate": "2026-05-07T12:00:00.000Z",
      "timeZoneGroupId": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the user account is active. |
| `allowedActions.canSubmitTimetrack` | boolean | Whether the user can submit time track. |
| `departmentId` | number | Department identifier. |
| `email` | string | Email address. |
| `firstName` | string | First name. |
| `fullName` | string | Full display name. |
| `hired` | date | Hire date. |
| `id` | number | Unique user identifier. |
| `lastName` | string | Last name. |
| `middleName` | string | Middle name or initial. |
| `releaseDate` | date | Release date. |
| `timeZoneGroupId` | number | Time zone group identifier. |
| `username` | string | Unique username. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /users` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

