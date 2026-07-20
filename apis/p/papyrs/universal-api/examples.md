# Papyrs Universal API Examples

These examples use the MindCloud API key and Papyrs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pages



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/list-pages?${params}`, {
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
      "category": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "id": "string",
      "is_public": 1,
      "slug": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Pages action reference](actions/list-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/papyrs/latest/actions/list-pages).

## Create Attachment Widget



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-attachment-widget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/create-attachment-widget', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "pageId": "string"
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
      "classname": "Ava Chen",
      "files": [
        {
          "filename": "Ava Chen",
          "size": 1,
          "url": "https://example.com",
          "vanity_size": "string"
        }
      ],
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Attachment Widget action reference](actions/create-attachment-widget.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/papyrs/latest/actions/create-attachment-widget).
