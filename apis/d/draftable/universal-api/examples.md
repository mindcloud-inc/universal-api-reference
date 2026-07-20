# Draftable Universal API Examples

These examples use the MindCloud API key and Draftable connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Comparisons

Retrieves your document comparisons from Draftable.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/draftable/latest/actions/list-comparisons?${params}`, {
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
      "comparisonType": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "failed": true,
      "identifier": "string",
      "left": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "public": true,
      "ready": true,
      "readyTime": "2026-05-07T12:00:00.000Z",
      "right": {
        "fileType": "string",
        "pageCount": 1,
        "sourceUrl": "https://example.com"
      },
      "viewerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Comparisons action reference](actions/list-comparisons.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/draftable/latest/actions/list-comparisons).

## Create Comparison

Creates a document comparison in Draftable.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/draftable/latest/actions/create-comparison" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "left.fileType": "csv",
  "right.fileType": "csv"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/draftable/latest/actions/create-comparison', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "left.fileType": "csv",
    "right.fileType": "csv"
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
      "comparisonType": "string",
      "creationTime": "2026-05-07T12:00:00.000Z",
      "identifier": "string",
      "left": {
        "fileType": "string",
        "sourceUrl": "https://example.com"
      },
      "ready": true,
      "right": {
        "fileType": "string",
        "sourceUrl": "https://example.com"
      },
      "viewerUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Comparison action reference](actions/create-comparison.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/draftable/latest/actions/create-comparison).
