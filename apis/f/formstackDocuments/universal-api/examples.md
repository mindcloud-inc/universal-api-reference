# Formstack Documents Universal API Examples

These examples use the MindCloud API key and Formstack Documents connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Documents

Retrieves a list of documents from Formstack Documents.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/list-documents?${params}`, {
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
      "active": "string",
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "output": "string",
      "size": "string",
      "sizeHeight": "string",
      "sizeWidth": "string",
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Documents action reference](actions/list-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formstackDocuments/latest/actions/list-documents).

## Combine Files

Combines files into one file in Formstack Documents.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/combine-files" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "files[].name": "Ava Chen",
  "output": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/formstackDocuments/latest/actions/combine-files', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "files[].name": "Ava Chen",
    "output": "string"
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

See the full [Combine Files action reference](actions/combine-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/formstackDocuments/latest/actions/combine-files).
