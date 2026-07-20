# Florm: Get Demo Token

Retrieves a demo access token from Florm.

```
GET https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-demo-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Florm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-demo-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/florm/latest/actions/get-demo-token?${params}`, {
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
      "expiresAccessToken": 1,
      "expiresRefreshToken": 1,
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessToken` | string | Demo access token. |
| `expiresAccessToken` | number | Minutes until the demo access token expires. |
| `expiresRefreshToken` | number | Minutes until the demo refresh token expires. |
| `refreshToken` | string | Demo refresh token. |

## Native endpoint

Through the native Florm API, this operation is `PUT /v1/auth/magic-links/demo` (base URL `https://api.florm.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-demo-token.md) for the provider-specific parameters and requirements.

