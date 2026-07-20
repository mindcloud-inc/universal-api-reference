# LinkAce Universal API Examples

These examples use the MindCloud API key and LinkAce connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links

Retrieves saved bookmark links from LinkAce.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-links?${params}`, {
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
      "next_page_url": "https://example.com",
      "path": "string",
      "per_page": "string",
      "prev_page_url": "https://example.com",
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkAce/latest/actions/list-links).

## Bulk Edit Links

Updates multiple bookmark links in LinkAce.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-edit-links" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/bulk-edit-links', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "check_disabled": true,
      "created_at": "string",
      "deleted_at": "string",
      "description": "string",
      "icon": "string",
      "id": 1,
      "status": 1,
      "title": "string",
      "updated_at": "string",
      "url": "https://example.com",
      "user_id": 1,
      "visibility": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Edit Links action reference](actions/bulk-edit-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkAce/latest/actions/bulk-edit-links).
