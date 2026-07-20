# swiDOC Universal API Examples

These examples use the MindCloud API key and swiDOC connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Document Metadata

Retrieves document metadata from swiDOC by document ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/get-document-metadata?${params}`, {
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
      "metadata": {
        "archivingEndDate": 1,
        "createdAt": 1,
        "description": "string",
        "fileName": "Ava Chen",
        "filePath": "string",
        "searchAttributes": [
          {}
        ],
        "tags": [
          "string"
        ]
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Document Metadata action reference](actions/get-document-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swiDOC/latest/actions/get-document-metadata).

## Archive Document

Archives a document in swiDOC.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/archive-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContent": "string",
  "metadata.fileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swiDOC/latest/actions/archive-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContent": "string",
    "metadata.fileName": "Ava Chen"
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
      "documentId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Archive Document action reference](actions/archive-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swiDOC/latest/actions/archive-document).
