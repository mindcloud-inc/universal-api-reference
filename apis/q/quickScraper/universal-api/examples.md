# Quick Scraper Universal API Examples

These examples use the MindCloud API key and Quick Scraper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Parse URL

Retrieves scraped page content from Quick Scraper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quickScraper/latest/actions/parse-url?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Parse URL action reference](actions/parse-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quickScraper/latest/actions/parse-url).
