# Supabase: Delete User

Deletes a user from Supabase Auth.

```
DELETE https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Supabase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabase/latest/actions/delete-user?${params}`, {
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

Through the native Supabase API, this operation is `DELETE /auth/v1/admin/users/:userId` (base URL `{{credentials.projectUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-user.md) for the provider-specific parameters and requirements.

