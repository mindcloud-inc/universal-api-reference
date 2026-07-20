# Advanced Scraper Universal API Examples

These examples use the MindCloud API key and Advanced Scraper connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scrape URL

Retrieves scraped data from a remote URL in Advanced Scraper.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/advancedScraper/latest/actions/scrape-url?${params}`, {
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
      "data": "string",
      "options": {},
      "request_headers": {},
      "response_headers": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Scrape URL action reference](actions/scrape-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/advancedScraper/latest/actions/scrape-url).
