# Enrich.so: Check Daily Scraping Limit

Retrieves daily scraping limits from Enrich.so.

```
GET https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-daily-scraping-limit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Enrich.so `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-daily-scraping-limit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/enrich/latest/actions/check-daily-scraping-limit?${params}`, {
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
      "limit": 1,
      "remaining": 1,
      "resetAt": "2026-05-07T12:00:00.000Z",
      "used": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limit` | number | Daily scraping limit. |
| `remaining` | number | Daily scraping calls remaining. |
| `resetAt` | date | Limit reset timestamp, when provided. |
| `used` | number | Daily scraping usage so far. |

## Native endpoint

Through the native Enrich.so API, this operation is `GET /company-follower/limit` (base URL `https://dev.enrich.so/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-daily-scraping-limit.md) for the provider-specific parameters and requirements.

