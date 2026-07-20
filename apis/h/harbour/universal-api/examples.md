# Harbour Universal API Examples

These examples use the MindCloud API key and Harbour connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Convert Document

Converts a Harbour document and returns a download URL.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document?connectionId=$CONNECTION_ID&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harbour/latest/actions/convert-document?${params}`, {
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
      "download_url": "https://example.com",
      "expires_at": 1
    }
  ],
  "meta": {}
}
```

See the full [Convert Document action reference](actions/convert-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harbour/latest/actions/convert-document).

## Annotate Document

Adds annotations to an existing document in Harbour.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harbour/latest/actions/annotate-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "document_id": "string",
  "field_values": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harbour/latest/actions/annotate-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "document_id": "string",
    "field_values": {}
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
      "download_url": "https://example.com",
      "expires_at": 1
    }
  ],
  "meta": {}
}
```

See the full [Annotate Document action reference](actions/annotate-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harbour/latest/actions/annotate-document).
