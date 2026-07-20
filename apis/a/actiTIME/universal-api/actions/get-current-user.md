# actiTIME: Get Current User

Retrieves the current user from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native actiTIME API, this operation is `GET /users/me` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

