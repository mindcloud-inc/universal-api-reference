# Evenium: Log In

Retrieves an access token from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-in?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/log-in?${params}`, {
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
      "accessToken": "string",
      "expiresIn": "string",
      "member": {},
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Evenium access token. |
| `expiresIn` | string | Token expiration duration/value from Evenium. |
| `member` | object | Authenticated member profile object. |
| `refreshToken` | string | Evenium refresh token. |

## Native endpoint

Through the native Evenium API, this operation is `POST /loginOAuth` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-in.md) for the provider-specific parameters and requirements.

