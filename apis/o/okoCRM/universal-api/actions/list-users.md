# OkoCRM: List users

Retrieves users from OkoCRM.

```
GET https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OkoCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/okoCRM/latest/actions/list-users?${params}`, {
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
      "act": 1,
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "date_born": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "last_visit": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `act` | number | Active status flag |
| `avatar_url` | string | Avatar URL |
| `created_at` | date | Created timestamp |
| `date_born` | date | Birth date |
| `deleted_at` | date | Deleted timestamp |
| `email` | string | Email address |
| `id` | number | OkoCRM user ID |
| `last_visit` | date | Last visit timestamp |
| `name` | string | Full name |
| `phone` | string | Phone number |
| `updated_at` | date | Updated timestamp |

## Native endpoint

Through the native OkoCRM API, this operation is `GET /users/` (base URL `https://api.okocrm.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

