# Whop: Get OAuth User Info

Retrieves your OAuth user information from Whop.

```
GET https://connect.mindcloud.co/v1/universal/whop/latest/actions/get-oauth-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whop/latest/actions/get-oauth-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whop/latest/actions/get-oauth-user-info?${params}`, {
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
      "emailVerified": true,
      "name": "Ava Chen",
      "picture": "string",
      "preferredUsername": "Ava Chen",
      "sub": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `name` | string |  |
| `picture` | string |  |
| `preferredUsername` | string |  |
| `sub` | string |  |

## Native endpoint

Through the native Whop API, this operation is `GET /oauth/userinfo` (base URL `https://api.whop.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-oauth-user-info.md) for the provider-specific parameters and requirements.

