# Supabase: List Users

Retrieves users from Supabase Auth administration.

```
GET https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/list-users?${params}`, {
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
      "aud": "string",
      "users": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "id": "string",
          "isAnonymous": true,
          "phone": "string",
          "role": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aud` | string |  |
| `users` | array<object> |  |
| `users[].createdAt` | date |  |
| `users[].email` | string |  |
| `users[].id` | string |  |
| `users[].isAnonymous` | boolean |  |
| `users[].phone` | string |  |
| `users[].role` | string |  |
| `users[].updatedAt` | date |  |

## Native endpoint

Through the native Supabase API, this operation is `GET /auth/v1/admin/users` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

