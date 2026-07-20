# Veryfi OCR Universal API Examples

These examples use the MindCloud API key and Veryfi OCR connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Documents

Finds documents in Veryfi OCR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/search-documents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/search-documents?${params}`, {
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
      "createdDate": "string",
      "id": 1,
      "status": "string",
      "total": 1,
      "updatedDate": "string",
      "vendor": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Documents action reference](actions/search-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veryfiOCR/latest/actions/search-documents).

## Add Tag To Document

Adds a tag to a document in Veryfi OCR.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/add-tag-to-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfiOCR/latest/actions/add-tag-to-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
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
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tag To Document action reference](actions/add-tag-to-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/veryfiOCR/latest/actions/add-tag-to-document).
