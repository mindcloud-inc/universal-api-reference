# TeamBook: List Users

Retrieves all user records from TeamBook.

```
GET https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeamBook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teamBook/latest/actions/list-users?${params}`, {
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
      "active": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "department": {
        "id": "string",
        "name": "Ava Chen"
      },
      "email": "ava@example.com",
      "end_date": "2026-05-07T12:00:00.000Z",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "phone_number": "string",
      "role": "string",
      "start_date": "2026-05-07T12:00:00.000Z",
      "tags": [
        {
          "color": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "teams": [
        {
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "time_zone": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | string |  |
| `created_at` | date |  |
| `department.id` | string |  |
| `department.name` | string |  |
| `email` | string |  |
| `end_date` | date |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `phone_number` | string |  |
| `role` | string |  |
| `start_date` | date |  |
| `tags[].color` | string |  |
| `tags[].id` | number |  |
| `tags[].name` | string |  |
| `teams[].id` | number |  |
| `teams[].name` | string |  |
| `time_zone` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TeamBook API, this operation is `GET /users` (base URL `https://web.teambookapp.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

