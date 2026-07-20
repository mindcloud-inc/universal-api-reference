# ScrapingBot Universal API Examples

These examples use the MindCloud API key and ScrapingBot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Google Search



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search?connectionId=$CONNECTION_ID&q=best%20web%20scraping%20tools%202025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "best web scraping tools 2025"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search?${params}`, {
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
      "creditsUsed": 1,
      "duration": "string",
      "organic": [
        {}
      ],
      "peopleAlsoAsk": [
        {}
      ],
      "relatedSearches": [
        {}
      ],
      "searchParameters": {},
      "statusCode": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Google Search action reference](actions/google-search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapingBot/latest/actions/google-search).
