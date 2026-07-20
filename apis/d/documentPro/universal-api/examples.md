# DocumentPro Universal API Examples

These examples use the MindCloud API key and DocumentPro connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workflows

Retrieves workflows from DocumentPro.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/list-workflows?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/list-workflows?${params}`, {
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
      "items": [
        {}
      ],
      "pagination_key": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Workflows action reference](actions/list-workflows.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentPro/latest/actions/list-workflows).

## Confirm Uploaded Document

Confirms a large uploaded document in DocumentPro.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/confirm-uploaded-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_extension": "string",
  "file_name": "Ava Chen",
  "upload_url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentPro/latest/actions/confirm-uploaded-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_extension": "string",
    "file_name": "Ava Chen",
    "upload_url": "https://example.com"
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
      "created_at": "string",
      "document_id": "string",
      "file_extension": "string",
      "file_name": "Ava Chen",
      "meta_tags": {},
      "num_pages": 1,
      "parser_runs": [
        {}
      ],
      "source_name": "Ava Chen",
      "updated_at": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Confirm Uploaded Document action reference](actions/confirm-uploaded-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentPro/latest/actions/confirm-uploaded-document).
