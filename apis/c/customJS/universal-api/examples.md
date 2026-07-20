# CustomJS Universal API Examples

These examples use the MindCloud API key and CustomJS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List HTML Pages

Retrieves hosted HTML pages from CustomJS.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customJS/latest/actions/list-html-pages?${params}`, {
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
      "cname": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "defaults": [
        {
          "path": "string",
          "type": "string",
          "values": {
            "layout": "string",
            "permalink": "https://example.com"
          }
        }
      ],
      "domain": "string",
      "id": "string",
      "metadata": {
        "permalink": "https://example.com"
      },
      "timezone": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List HTML Pages action reference](actions/list-html-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customJS/latest/actions/list-html-pages).

## Capture Screenshot

Captures a website screenshot in CustomJS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/customJS/latest/actions/capture-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/customJS/latest/actions/capture-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.url": "https://example.com"
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
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Capture Screenshot action reference](actions/capture-screenshot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/customJS/latest/actions/capture-screenshot).
