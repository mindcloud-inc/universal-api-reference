# Siteleaf: Get Authenticated User

Retrieves the authenticated user from Siteleaf.

```
GET https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Siteleaf `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/get-authenticated-user?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "fullname": "Ava Chen",
      "id": "string",
      "lastname": "Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `fullname` | string |  |
| `id` | string |  |
| `lastname` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Siteleaf API, this operation is `GET /users/me` (base URL `https://api.siteleaf.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

