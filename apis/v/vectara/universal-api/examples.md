# Vectara Universal API Examples

These examples use the MindCloud API key and Vectara connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Corpora

Retrieves a list of corpora from Vectara.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectara/latest/actions/list-corpora?${params}`, {
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
      "corpora": [
        {}
      ],
      "metadata": {}
    }
  ],
  "meta": {}
}
```

See the full [List Corpora action reference](actions/list-corpora.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectara/latest/actions/list-corpora).

## Add Document

Adds a document to a Vectara corpus for indexing.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectara/latest/actions/add-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "corpusKey": "string",
  "type": "0",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectara/latest/actions/add-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "corpusKey": "string",
    "type": "0",
    "id": "string"
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
      "extraction_usage": {},
      "id": "string",
      "images": [
        {}
      ],
      "metadata": {},
      "parts": [
        {}
      ],
      "storage_usage": {},
      "tables": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Document action reference](actions/add-document.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectara/latest/actions/add-document).
