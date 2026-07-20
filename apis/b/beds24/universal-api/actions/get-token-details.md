# Beds24: Get Token Details

Retrieves token details and diagnostics from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/get-token-details?${params}`, {
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
      "diagnostics": {},
      "token": {},
      "validToken": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `diagnostics` | object | Diagnostic details returned by Beds24 for the current request. |
| `token` | object | Metadata about the current Beds24 access token. |
| `validToken` | boolean | Whether the supplied Beds24 access token is valid. |

## Native endpoint

Through the native Beds24 API, this operation is `GET /authentication/details` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-details.md) for the provider-specific parameters and requirements.

