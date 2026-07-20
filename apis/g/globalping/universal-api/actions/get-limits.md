# Globalping: Get Limits

Retrieves current Globalping usage limits.

```
GET https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Globalping `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits?${params}`, {
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
      "credits": {},
      "rateLimit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | object | Remaining Globalping credit balance for the authenticated user. |
| `rateLimit` | object | Current measurement rate limit information for the authenticated user. |

## Native endpoint

Through the native Globalping API, this operation is `GET /v1/limits` (base URL `https://api.globalping.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-limits.md) for the provider-specific parameters and requirements.

