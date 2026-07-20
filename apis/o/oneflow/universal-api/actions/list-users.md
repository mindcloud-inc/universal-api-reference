# Oneflow: List Users

Retrieves users from Oneflow.

```
GET https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/list-users?${params}`, {
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
      "_links": {},
      "active": true,
      "email": "ava@example.com",
      "id": 1,
      "is_admin": true,
      "name": "Ava Chen",
      "phone_number": "string",
      "state": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Links related to the user resource. |
| `active` | boolean | Whether the user is active. |
| `email` | string | The user's email address. |
| `id` | number | The Oneflow user ID. |
| `is_admin` | boolean | Whether the user is an administrator. |
| `name` | string | The user's full name. |
| `phone_number` | string | The user's phone number. |
| `state` | string | The user's account state. |
| `title` | string | The user's title. |

## Native endpoint

Through the native Oneflow API, this operation is `GET /users` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

