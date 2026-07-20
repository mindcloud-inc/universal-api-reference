# BuildBetter Universal API Examples

These examples use the MindCloud API key and BuildBetter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Recent Calls



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/list-recent-calls?${params}`, {
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
      "display_ts": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "short_summary": "string",
      "source": "string",
      "transcript_status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Recent Calls action reference](actions/list-recent-calls.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildBetter/latest/actions/list-recent-calls).

## Create Company



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Example Corp"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/create-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Example Corp"
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
      "color": "string",
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "photo_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Company action reference](actions/create-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/buildBetter/latest/actions/create-company).
