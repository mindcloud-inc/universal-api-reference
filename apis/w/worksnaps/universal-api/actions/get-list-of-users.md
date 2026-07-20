# Worksnaps: Get list of users

Retrieves users from Worksnaps.

```
GET https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-list-of-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-list-of-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/get-list-of-users?${params}`, {
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
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "is_in_daylight_time": true,
      "last_name": "Chen",
      "login": "string",
      "password": "string",
      "timezone_id": 1,
      "timezone_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | the email of the user |
| `first_name` | string | the first name of the user |
| `id` | number | the ID of the user |
| `is_in_daylight_time` | boolean | whether the user is in daylight saving time (true or false) |
| `last_name` | string | last name of the user |
| `login` | string | the login of the user |
| `password` | string | the password of the user |
| `timezone_id` | number | the timezone ID of the user |
| `timezone_name` | string | the timezone name of the user |

## Native endpoint

Through the native Worksnaps API, this operation is `GET /users.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-of-users.md) for the provider-specific parameters and requirements.

