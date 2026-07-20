# Didit Universal API Examples

These examples use the MindCloud API key and Didit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sessions

Retrieves sessions from Didit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/didit/latest/actions/list-sessions?${params}`, {
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
      "sessionId": "string",
      "status": "string",
      "vendorData": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sessions action reference](actions/list-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/didit/latest/actions/list-sessions).

## Add to Blocklist

Adds an entry to the Didit blocklist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/didit/latest/actions/add-to-blocklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/didit/latest/actions/add-to-blocklist', {
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

See the full [Add to Blocklist action reference](actions/add-to-blocklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/didit/latest/actions/add-to-blocklist).
