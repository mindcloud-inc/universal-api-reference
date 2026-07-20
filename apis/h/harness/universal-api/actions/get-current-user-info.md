# Harness: Get Current User Info

Retrieves the current user from Harness.

```
GET https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info?${params}`, {
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
      "admin": true,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean |  |
| `email` | string |  |
| `name` | string |  |
| `username` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Harness API, this operation is `GET /ng/api/user/currentUser` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-info.md) for the provider-specific parameters and requirements.

