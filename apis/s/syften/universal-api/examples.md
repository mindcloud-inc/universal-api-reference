# Syften Universal API Examples

These examples use the MindCloud API key and Syften connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Info

Retrieves account details and plan information from Syften.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/syften/latest/actions/get-info?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "plan": {},
      "quota_counters": {},
      "stats": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Info action reference](actions/get-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syften/latest/actions/get-info).

## Set Filters

Updates the saved filter list in Syften.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/syften/latest/actions/set-filters" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filters[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syften/latest/actions/set-filters', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filters[]": ["string"]
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

See the full [Set Filters action reference](actions/set-filters.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/syften/latest/actions/set-filters).
