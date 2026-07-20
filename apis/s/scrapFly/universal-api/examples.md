# ScrapFly Universal API Examples

These examples use the MindCloud API key and ScrapFly connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scrape URL

Retrieves a scraped page from ScrapFly.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fweb-scraping.dev%2Fproduct%2F1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://web-scraping.dev/product/1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url?${params}`, {
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
      "config": {
        "method": "string",
        "project": "string",
        "url": "https://example.com"
      },
      "result": {
        "contentType": "string",
        "logUrl": "https://example.com",
        "statusCode": 1,
        "success": true,
        "url": "https://example.com"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Scrape URL action reference](actions/scrape-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapFly/latest/actions/scrape-url).

## Scrape URL via PATCH

Updates an existing page scrape in ScrapFly.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url-via-patch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://httpbin.dev/anything"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scrapFly/latest/actions/scrape-url-via-patch', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://httpbin.dev/anything"
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
      "config": {
        "method": "string",
        "project": "string",
        "url": "https://example.com"
      },
      "result": {
        "contentType": "string",
        "logUrl": "https://example.com",
        "statusCode": 1,
        "success": true,
        "url": "https://example.com"
      },
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Scrape URL via PATCH action reference](actions/scrape-url-via-patch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scrapFly/latest/actions/scrape-url-via-patch).
