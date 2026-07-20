# Supabase: Update User

Updates a user in Supabase Auth.

```
PUT https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabase/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailConfirmedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isAnonymous": true,
      "phone": "string",
      "phoneConfirmedAt": "2026-05-07T12:00:00.000Z",
      "role": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aud` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailConfirmedAt` | date |  |
| `id` | string |  |
| `isAnonymous` | boolean |  |
| `phone` | string |  |
| `phoneConfirmedAt` | date |  |
| `role` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Supabase API, this operation is `PUT /auth/v1/admin/users/:userId` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

