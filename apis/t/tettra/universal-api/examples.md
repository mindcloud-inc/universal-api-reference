# Tettra Universal API Examples

These examples use the MindCloud API key and Tettra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Pages

Finds pages in Tettra by search term.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages?${params}`, {
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
      "pages": [
        {
          "category": {
            "id": 1,
            "name": "Ava Chen",
            "url": "https://example.com"
          },
          "content": "string",
          "id": 1,
          "owner": "string",
          "title": "string",
          "updated_at": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com"
        }
      ],
      "query": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Search Pages action reference](actions/search-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tettra/latest/actions/search-pages).

## Create Category

Creates a new category in Tettra.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tettra/latest/actions/create-category', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
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
      "category": {
        "color": "string",
        "description": "string",
        "icon": "string",
        "id": 1,
        "name": "Ava Chen",
        "visibility": 1
      },
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Category action reference](actions/create-category.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tettra/latest/actions/create-category).
