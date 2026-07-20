# Cinode: Get Access Token

Retrieves an access token from Cinode.

```
GET https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-access-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cinode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-access-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cinode/latest/actions/get-access-token?${params}`, {
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
      "access_token": "string",
      "refresh_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | Short-lived bearer token returned by Cinode for API requests. |
| `refresh_token` | string | Refresh token returned by Cinode alongside the bearer token. |

## Native endpoint

Through the native Cinode API, this operation is `GET /token` (base URL `https://api.cinode.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-access-token.md) for the provider-specific parameters and requirements.

