# JotUrl: Get Watchdog Stats

Retrieves watchdog stats from JotUrl.

```
GET https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JotUrl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jotUrl/latest/actions/get-watchdog-stats?${params}`, {
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
      "spiders": "string",
      "stats": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `spiders` | string |  |
| `stats` | string |  |

## Native endpoint

Through the native JotUrl API, this operation is `GET /watchdogs/stats` (base URL `https://joturl.com/a/i1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-watchdog-stats.md) for the provider-specific parameters and requirements.

