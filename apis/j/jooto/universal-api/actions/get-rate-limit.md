# Jooto: Get Rate Limit

Retrieves current API rate limit details from Jooto.

```
GET https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-rate-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jooto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-rate-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jooto/latest/actions/get-rate-limit?${params}`, {
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
      "get": {
        "limit": 1,
        "remaining": 1,
        "reset": 1
      },
      "update": {
        "limit": 1,
        "remaining": 1,
        "reset": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `get.limit` | number | Maximum read requests allowed in the current window. |
| `get.remaining` | number | Remaining read requests in the current window. |
| `get.reset` | number | Unix timestamp when the read request window resets. |
| `update.limit` | number | Maximum update requests allowed in the current window. |
| `update.remaining` | number | Remaining update requests in the current window. |
| `update.reset` | number | Unix timestamp when the update request window resets. |

## Native endpoint

Through the native Jooto API, this operation is `GET /api/public/v1/rate_limit` (base URL `https://app.jooto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rate-limit.md) for the provider-specific parameters and requirements.

