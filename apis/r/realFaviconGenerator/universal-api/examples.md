# RealFaviconGenerator Universal API Examples

These examples use the MindCloud API key and RealFaviconGenerator connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List change log



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/list-change-log?${params}`, {
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
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "importance": "string",
      "relevance": {},
      "updateOrNot": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List change log action reference](actions/list-change-log.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realFaviconGenerator/latest/actions/list-change-log).

## Start favicon generation



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/start-favicon-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/realFaviconGenerator/latest/actions/start-favicon-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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

See the full [Start favicon generation action reference](actions/start-favicon-generation.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/realFaviconGenerator/latest/actions/start-favicon-generation).
