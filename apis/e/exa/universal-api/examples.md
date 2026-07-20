# Exa Universal API Examples

These examples use the MindCloud API key and Exa connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search

Finds relevant search results in Exa.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/search?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/search?${params}`, {
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
      "author": "string",
      "entities": [
        {}
      ],
      "extras": {},
      "favicon": "string",
      "highlights": [
        "string"
      ],
      "highlightScores": [
        1
      ],
      "id": "string",
      "image": "string",
      "publishedDate": "2026-05-07T12:00:00.000Z",
      "score": 1,
      "subpages": [
        {}
      ],
      "summary": "string",
      "text": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Search action reference](actions/search.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/exa/latest/actions/search).

## Cancel Webset

Cancels a running webset in Exa.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/cancel-webset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
      "createdAt": "string",
      "enrichments": "string",
      "excludes": "string",
      "externalId": "string",
      "id": "string",
      "imports": "string",
      "metadata": "string",
      "monitors": "string",
      "object": "string",
      "searches": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel Webset action reference](actions/cancel-webset.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/exa/latest/actions/cancel-webset).
