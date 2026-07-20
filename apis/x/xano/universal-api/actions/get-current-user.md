# Xano: Get Current User

Retrieves the authenticated user from Xano.

```
GET https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Xano `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xano/latest/actions/get-current-user?${params}`, {
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
      "email": "ava@example.com",
      "extras": {
        "instance": {
          "display": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `extras.instance.display` | string |  |
| `extras.instance.id` | number |  |
| `extras.instance.name` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Xano API, this operation is `GET /api%3Ameta/auth/me` (base URL `https://x8ki-letl-twmt.n7.xano.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

