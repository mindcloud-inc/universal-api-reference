# KlipLink Universal API Examples

These examples use the MindCloud API key and KlipLink connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Links



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/list-links?${params}`, {
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
      "links": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Links action reference](actions/list-links.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/klipLink/latest/actions/list-links).

## Create Link



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/create-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/klipLink/latest/actions/create-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com"
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
      "clicks": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "destination_url": "https://example.com",
      "id": "string",
      "short_url": "https://example.com",
      "success": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Link action reference](actions/create-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/klipLink/latest/actions/create-link).
