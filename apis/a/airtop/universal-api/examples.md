# Airtop Universal API Examples

These examples use the MindCloud API key and Airtop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sessions

Finds sessions in Airtop by ID or status.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/list-sessions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtop/latest/actions/list-sessions?${params}`, {
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

See the full [List Sessions action reference](actions/list-sessions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airtop/latest/actions/list-sessions).

## Click

Clicks an element in a specific Airtop window.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/click" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string",
  "windowId": "string",
  "elementDescription": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airtop/latest/actions/click', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string",
    "windowId": "string",
    "elementDescription": "string"
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

See the full [Click action reference](actions/click.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/airtop/latest/actions/click).
