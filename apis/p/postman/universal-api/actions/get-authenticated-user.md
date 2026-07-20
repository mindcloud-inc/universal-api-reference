# Postman: Get Authenticated User

Retrieves authenticated user details and usage limits from Postman.

```
GET https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postman/latest/actions/get-authenticated-user?${params}`, {
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
      "operations": [
        {
          "limit": 1,
          "name": "Ava Chen",
          "usage": 1
        }
      ],
      "user": {
        "email": "ava@example.com",
        "id": 1,
        "username": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `operations[].limit` | number |  |
| `operations[].name` | string |  |
| `operations[].usage` | number |  |
| `user.email` | string |  |
| `user.id` | number |  |
| `user.username` | string |  |

## Native endpoint

Through the native Postman API, this operation is `GET /me` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

