# Brand.dev Universal API Examples

These examples use the MindCloud API key and Brand.dev connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scrape Raw HTML from a URL

Retrieves raw HTML from a URL using Brand.dev.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-raw-html-from-a-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/branddev/latest/actions/scrape-raw-html-from-a-url?${params}`, {
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
      "html": "string",
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Scrape Raw HTML from a URL action reference](actions/scrape-raw-html-from-a-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/branddev/latest/actions/scrape-raw-html-from-a-url).

## Prefetch Brand Data by Email

Prefetches brand data in Brand.dev by email.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/branddev/latest/actions/prefetch-brand-data-by-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/branddev/latest/actions/prefetch-brand-data-by-email', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com"
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
      "domain": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Prefetch Brand Data by Email action reference](actions/prefetch-brand-data-by-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/branddev/latest/actions/prefetch-brand-data-by-email).
