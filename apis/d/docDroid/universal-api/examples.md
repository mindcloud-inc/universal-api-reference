# DocDroid Universal API Examples

These examples use the MindCloud API key and DocDroid connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List My Documents

Retrieves your uploaded documents from DocDroid.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/list-my-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/list-my-documents?${params}`, {
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
      "allowAiChat": true,
      "allowCopyText": true,
      "allowDownload": true,
      "allowEmbed": "string",
      "allowSearchEnginesIndex": true,
      "created": "2026-05-07T12:00:00.000Z",
      "downloads": 1,
      "ext": "string",
      "filename": "Ava Chen",
      "hash": "string",
      "id": "string",
      "links": [
        {
          "rel": "https://example.com",
          "type": "https://example.com",
          "uri": "https://example.com"
        }
      ],
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "user": {
        "id": 1
      },
      "views": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

See the full [List My Documents action reference](actions/list-my-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docDroid/latest/actions/list-my-documents).

## Create Webhook

Creates a new webhook in DocDroid.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "document.created",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docDroid/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "document.created",
    "targetUrl": "https://example.com"
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
      "created": "2026-05-07T12:00:00.000Z",
      "event": "string",
      "id": 1,
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docDroid/latest/actions/create-webhook).
