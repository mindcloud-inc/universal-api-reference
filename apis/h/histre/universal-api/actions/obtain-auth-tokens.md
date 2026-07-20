# Histre: Obtain Auth Tokens

Obtains authentication tokens from Histre for API access.

```
GET https://connect.mindcloud.co/v1/universal/histre/latest/actions/obtain-auth-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/obtain-auth-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/obtain-auth-tokens?${params}`, {
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
      "access": "string",
      "refresh": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access` | string | Short-lived JWT access token returned by Histre login. |
| `refresh` | string | Refresh token returned by Histre login. |

## Native endpoint

Through the native Histre API, this operation is `POST /api/v1/auth_token/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/obtain-auth-tokens.md) for the provider-specific parameters and requirements.

