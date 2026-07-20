# DocRaptor Universal API Examples

These examples use the MindCloud API key and DocRaptor connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves paginated document records from DocRaptor.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/list-documents?${params}`, {
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
      "async": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_at_v2": "2026-05-07T12:00:00.000Z",
      "document_type": "string",
      "domain_id": 1,
      "id": 1,
      "ip_address": "string",
      "javascript": true,
      "name": "Ava Chen",
      "tag": "string",
      "test": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "updated_at_v2": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docRaptor/latest/actions/list-documents).

## Create Async PDF from HTML Content

Creates an async PDF in DocRaptor from HTML content.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-async-pdf-from-html-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docRaptor/latest/actions/create-async-pdf-from-html-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentContent": "string"
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
      "status_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Async PDF from HTML Content action reference](actions/create-async-pdf-from-html-content.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docRaptor/latest/actions/create-async-pdf-from-html-content).
