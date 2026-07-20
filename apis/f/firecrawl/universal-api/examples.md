# Firecrawl Universal API Examples

These examples use the MindCloud API key and Firecrawl connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scrape URL

Scrapes a single URL with Firecrawl.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/scrape-url?${params}`, {
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
      "markdown": "string",
      "metadata": {
        "cachedAt": "2026-05-07T12:00:00.000Z",
        "cacheState": "string",
        "concurrencyLimited": true,
        "contentType": "string",
        "creditsUsed": 1,
        "language": "string",
        "proxyUsed": "string",
        "scrapeId": "string",
        "sourceURL": "https://example.com",
        "statusCode": 1,
        "title": "string",
        "url": "https://example.com",
        "viewport": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Scrape URL action reference](actions/scrape-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firecrawl/latest/actions/scrape-url).

## Batch Scrape URLs

Creates a batch scrape job in Firecrawl.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/batch-scrape-urls" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firecrawl/latest/actions/batch-scrape-urls', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls[]": ["https://example.com"]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "invalidURLs": [
        "https://example.com"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Batch Scrape URLs action reference](actions/batch-scrape-urls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firecrawl/latest/actions/batch-scrape-urls).
