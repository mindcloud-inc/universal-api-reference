# NextLead Universal API Examples

These examples use the MindCloud API key and NextLead connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Identify Organization

Verifies your API key and retrieves your NextLead organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/identify-organization?${params}`, {
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
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Identify Organization action reference](actions/identify-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextLead/latest/actions/identify-organization).

## Create Action

Creates a new task in NextLead.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "column": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nextLead/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "column": "string"
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
      "message": "string",
      "project": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Action action reference](actions/create-action.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nextLead/latest/actions/create-action).
