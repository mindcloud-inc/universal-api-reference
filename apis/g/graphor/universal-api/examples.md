# Graphor Universal API Examples

These examples use the MindCloud API key and Graphor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sources

Retrieves sources from your Graphor project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphor/latest/actions/list-sources?${params}`, {
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
      "fileId": "string",
      "fileName": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sources action reference](actions/list-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/graphor/latest/actions/list-sources).

## Crawl URL Sources

Creates a new source in Graphor by crawling a URL.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/graphor/latest/actions/crawl-url-sources" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/graphor/latest/actions/crawl-url-sources', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
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
      "buildId": "string",
      "error": "string",
      "message": "string",
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Crawl URL Sources action reference](actions/crawl-url-sources.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/graphor/latest/actions/crawl-url-sources).
