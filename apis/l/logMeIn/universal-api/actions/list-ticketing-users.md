# LogMeIn: List Ticketing Users

Retrieves available ticketing users from LogMeIn.

```
GET https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-ticketing-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-ticketing-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/list-ticketing-users?${params}`, {
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
| `serviceId` | string | no | Optional service identifier. Leave blank to return users from all services. |
| `userType` | string | no | User type filter. |
| `limit` | number | no | Number of users to return. |
| `keyword` | string | no | Filter users by first name, last name, or email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "userType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `userType` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `GET /goto-resolve-ticketing/v1/users` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticketing-users.md) for the provider-specific parameters and requirements.

