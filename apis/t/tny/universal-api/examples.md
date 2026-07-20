# Tny Universal API Examples

These examples use the MindCloud API key and Tny connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links

Retrieves short links from Tny.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tny/latest/actions/list-links?${params}`, {
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
      "clickCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customDomain": "string",
      "id": "string",
      "longUrl": "https://example.com",
      "shortUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tny/latest/actions/list-links).

## Bulk Create Short Links

Creates multiple shortened links in Tny.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tny/latest/actions/bulk-create-short-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "links": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tny/latest/actions/bulk-create-short-links', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "links": {}
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
      "created": 1,
      "errors": [
        {}
      ],
      "failed": 1,
      "results": [
        {}
      ],
      "success": true,
      "tier": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Create Short Links action reference](actions/bulk-create-short-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tny/latest/actions/bulk-create-short-links).
