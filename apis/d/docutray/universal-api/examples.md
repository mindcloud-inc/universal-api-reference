# Docutray Universal API Examples

These examples use the MindCloud API key and Docutray connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Document Types



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docutray/latest/actions/list-document-types?${params}`, {
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
      "codeType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "isDraft": true,
      "isPublic": true,
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Document Types action reference](actions/list-document-types.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docutray/latest/actions/list-document-types).

## Bulk Upload Knowledge Base Documents



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/bulk-upload-knowledge-base-documents" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "documents[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/bulk-upload-knowledge-base-documents', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "documents[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Bulk Upload Knowledge Base Documents action reference](actions/bulk-upload-knowledge-base-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docutray/latest/actions/bulk-upload-knowledge-base-documents).
