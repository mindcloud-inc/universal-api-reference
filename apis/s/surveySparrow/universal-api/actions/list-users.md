# SurveySparrow: List Users

Retrieves all users from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-users?${params}`, {
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
      "admin": true,
      "agency_owner": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "current_user": true,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "owner": true,
      "phone": "string",
      "profile_pic": "string",
      "role_id": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean |  |
| `agency_owner` | boolean |  |
| `created_at` | date |  |
| `current_user` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | boolean |  |
| `phone` | string |  |
| `profile_pic` | string |  |
| `role_id` | number |  |
| `verified` | boolean |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /users` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

