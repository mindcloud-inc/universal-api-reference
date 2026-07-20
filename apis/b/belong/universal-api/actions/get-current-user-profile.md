# Belong: Get Current User Profile

Retrieves the current user profile from Belong.

```
GET https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Belong `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/belong/latest/actions/get-current-user-profile?${params}`, {
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
      "biography": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": {},
      "phoneNumber": {},
      "proGaslessCollection": true,
      "username": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `biography` | string | Profile biography text. |
| `email` | string | Primary email address for the authenticated user. |
| `id` | string | Belong user ID. |
| `name` | object | Structured name object returned by Belong. |
| `phoneNumber` | object |  |
| `proGaslessCollection` | boolean | Whether gasless collection support is enabled for the user. |
| `username` | object |  |

## Native endpoint

Through the native Belong API, this operation is `GET /me` (base URL `https://api.belong.net/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-profile.md) for the provider-specific parameters and requirements.

