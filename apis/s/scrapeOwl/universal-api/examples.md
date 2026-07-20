# ScrapeOwl Universal API Examples

These examples use the MindCloud API key and ScrapeOwl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Usage



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

Example response:

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

See the full [Get Usage action reference](actions/get-usage.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapeOwl/latest/actions/get-usage).
