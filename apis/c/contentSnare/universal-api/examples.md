# Content Snare Universal API Examples

These examples use the MindCloud API key and Content Snare connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Requests

Retrieves requests from Content Snare.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-requests?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/list-requests?${params}`, {
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Requests action reference](actions/list-requests.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentSnare/latest/actions/list-requests).

## Approve All Submitted Fields

Approves all submitted fields for a request in Content Snare.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/approve-all-submitted-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentSnare/latest/actions/approve-all-submitted-fields', {
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
  "data": [],
  "meta": {}
}
```

See the full [Approve All Submitted Fields action reference](actions/approve-all-submitted-fields.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/contentSnare/latest/actions/approve-all-submitted-fields).
