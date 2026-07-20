# Siteleaf Universal API Examples

These examples use the MindCloud API key and Siteleaf connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves sites from Siteleaf.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/list-sites?${params}`, {
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
        [
          {}
        ]
      ],
      "domain": "string",
      "id": "string",
      "jobs": {
        "preview": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        },
        "publish": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        },
        "sync": {
          "id": "string",
          "last_at": "2026-05-07T12:00:00.000Z",
          "last_error": "string",
          "last_id": "string"
        }
      },
      "metadata": {},
      "storage_limit": 1,
      "storage_used": 1,
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

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/siteleaf/latest/actions/list-sites).

## Create Collection

Creates a new collection in Siteleaf.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/siteleaf/latest/actions/create-collection', {
  method: 'POST',
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "directory": "string",
      "id": "string",
      "metadata": {},
      "output": true,
      "path": "string",
      "permalink": "https://example.com",
      "site_id": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Collection action reference](actions/create-collection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/siteleaf/latest/actions/create-collection).
