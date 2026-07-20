# Docparser Universal API Examples

These examples use the MindCloud API key and Docparser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Data Of Multiple Documents

Retrieves parsed data for multiple Docparser documents.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents?connectionId=$CONNECTION_ID&parserId=tiumtyrcddpn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parserId": "tiumtyrcddpn"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docparser/latest/actions/get-data-of-multiple-documents?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Data Of Multiple Documents action reference](actions/get-data-of-multiple-documents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docparser/latest/actions/get-data-of-multiple-documents).

## Fetch Document From URL

Fetches a document from a URL into a Docparser parser.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docparser/latest/actions/fetch-document-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parserId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docparser/latest/actions/fetch-document-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parserId": "string",
    "url": "https://example.com"
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
      "message": "string",
      "parserId": "string",
      "remoteId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Fetch Document From URL action reference](actions/fetch-document-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/docparser/latest/actions/fetch-document-from-url).
