# Beds24: Refresh Access Token

Retrieves an access token from a Beds24 refresh token.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/refresh-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/refresh-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/refresh-access-token?${params}`, {
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
      "expiresIn": 1,
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiresIn` | number |  |
| `token` | string |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /authentication/token` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-access-token.md) for the provider-specific parameters and requirements.

