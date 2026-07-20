# TLY Link Shortener Universal API Examples

These examples use the MindCloud API key and TLY Link Shortener connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Short Links

Retrieves short links from TLY Link Shortener.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/list-short-links?${params}`, {
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
      "current_page": 1,
      "data": [
        {}
      ],
      "first_page_url": "https://example.com",
      "from": 1,
      "last_page": 1,
      "last_page_url": "https://example.com",
      "links": [
        {}
      ],
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Short Links action reference](actions/list-short-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tLYLinkShortener/latest/actions/list-short-links).

## Bulk Shorten Links

Creates short links in bulk in TLY Link Shortener.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-shorten-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links[]": [
    "https://example.com"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/bulk-shorten-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links[]": ["https://example.com"]
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
      "response": true
    }
  ],
  "meta": {}
}
```

See the full [Bulk Shorten Links action reference](actions/bulk-shorten-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tLYLinkShortener/latest/actions/bulk-shorten-links).
