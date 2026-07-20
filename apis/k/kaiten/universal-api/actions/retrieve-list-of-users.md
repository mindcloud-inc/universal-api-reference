# Kaiten: Retrieve List of Users

Retrieves users from Kaiten.

```
GET https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kaiten `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kaiten/latest/actions/retrieve-list-of-users?${params}`, {
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
      "activated": true,
      "avatar_initials_url": "https://example.com",
      "avatar_uploaded_url": "https://example.com",
      "company_id": 1,
      "default_space_id": 1,
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "last_request_date": "2026-05-07T12:00:00.000Z",
      "permissions": 1,
      "role": 1,
      "uid": "string",
      "user_id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated` | boolean |  |
| `avatar_initials_url` | string |  |
| `avatar_uploaded_url` | string |  |
| `company_id` | number |  |
| `default_space_id` | number |  |
| `email` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `last_request_date` | date |  |
| `permissions` | number |  |
| `role` | number |  |
| `uid` | string |  |
| `user_id` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Kaiten API, this operation is `GET /users` (base URL `https://{{credentials.companyDomain}}.kaiten.ru/api/latest`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/retrieve-list-of-users.md) for the provider-specific parameters and requirements.

