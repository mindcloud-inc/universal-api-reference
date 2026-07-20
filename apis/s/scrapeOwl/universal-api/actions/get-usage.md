# ScrapeOwl: Get Usage



```
GET https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapeOwl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeOwl/latest/actions/get-usage?${params}`, {
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
      "concurrency_limit": 1,
      "concurrent_requests": 1,
      "credits": 1,
      "credits_used": 1,
      "failed_requests": 1,
      "requests": 1,
      "successful_requests": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `concurrency_limit` | number | Allowed concurrent request count. |
| `concurrent_requests` | number | Current concurrent request count. |
| `credits` | number | Current available credits. |
| `credits_used` | number | Credits used. |
| `failed_requests` | number | Failed request count. |
| `requests` | number | Total requests. |
| `successful_requests` | number | Successful request count. |

## Native endpoint

Through the native ScrapeOwl API, this operation is `GET /usage` (base URL `https://api.scrapeowl.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

