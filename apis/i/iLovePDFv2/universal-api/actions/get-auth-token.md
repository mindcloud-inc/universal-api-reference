# iLovePDFv2: Get Auth Token

Retrieves an auth token from iLovePDFv2.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-auth-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-auth-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/get-auth-token?${params}`, {
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
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `token` | string | Short-lived iLoveAPI JWT token. |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `POST /auth` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-token.md) for the provider-specific parameters and requirements.

