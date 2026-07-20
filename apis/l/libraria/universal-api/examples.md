# Libraria Universal API Examples

These examples use the MindCloud API key and Libraria connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Document

Get a document from a library.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document?connectionId=$CONNECTION_ID&libraryId=string&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "libraryId": "string",
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/libraria/latest/actions/get-document?${params}`, {
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
      "createdAt": "string",
      "id": "string",
      "scrapeStatus": "string",
      "sourceUrl": "https://example.com",
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Document action reference](actions/get-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/libraria/latest/actions/get-document).

## Add Document

Add a new document to your library via scraping or raw text.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/libraria/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "libraryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/libraria/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "libraryId": "string"
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
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Document action reference](actions/add-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/libraria/latest/actions/add-document).
