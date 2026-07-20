# UseINBOX: Get Token

Retrieves an access token from UseINBOX.

```
GET https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-token?${params}`, {
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
      "expires_in": 1,
      "refresh_token": "string",
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_token` | string | Bearer access token returned by UseINBOX. |
| `expires_in` | number | Token lifetime in seconds. |
| `refresh_token` | string | Refresh token when returned by UseINBOX. |
| `token_type` | string | Token type returned by UseINBOX. |

## Native endpoint

Through the native UseINBOX API, this operation is `POST /token` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token.md) for the provider-specific parameters and requirements.

