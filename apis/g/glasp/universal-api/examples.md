# Glasp Universal API Examples

These examples use the MindCloud API key and Glasp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Highlights

Retrieves your Glasp highlights with optional filtering and pagination.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glasp/latest/actions/export-highlights?${params}`, {
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
      "count": 1,
      "nextPageCursor": "string",
      "results": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

See the full [Export Highlights action reference](actions/export-highlights.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/glasp/latest/actions/export-highlights).

## Create Highlights

Creates new highlights in your Glasp account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/glasp/latest/actions/create-highlights" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "highlights[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glasp/latest/actions/create-highlights', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "highlights[]": [{}]
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
      "category": "string",
      "domain": "string",
      "glaspUrl": "https://example.com",
      "highlights": [
        [
          {}
        ]
      ],
      "id": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Highlights action reference](actions/create-highlights.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/glasp/latest/actions/create-highlights).
