# Cerbo: List Users

Retrieves user records from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-users?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | If a non-empty value is passed the system will include deleted/suspended users in the return. If the argument is omitted only active users will be returned. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "created": "string",
      "displayNameForAppointments": "Ava Chen",
      "displayNameForMessages": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasCalendar": true,
      "id": "string",
      "isResource": true,
      "lastName": "Chen",
      "loginActive": true,
      "middleName": "Ava Chen",
      "npi": "string",
      "object": "string",
      "prefix": "string",
      "suffix": "string",
      "userNotes": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | string |  |
| `displayNameForAppointments` | string |  |
| `displayNameForMessages` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasCalendar` | boolean |  |
| `id` | string |  |
| `isResource` | boolean |  |
| `lastName` | string |  |
| `loginActive` | boolean |  |
| `middleName` | string |  |
| `npi` | string |  |
| `object` | string |  |
| `prefix` | string |  |
| `suffix` | string |  |
| `userNotes` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /users` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

