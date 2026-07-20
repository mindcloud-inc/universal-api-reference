# HelloLeads Universal API Examples

These examples use the MindCloud API key and HelloLeads connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lead Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/list-lead-lists?${params}`, {
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
      "created": "string",
      "list_key": "string",
      "modified": "string",
      "name": "Ava Chen",
      "owner": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Lead Lists action reference](actions/list-lead-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helloLeads/latest/actions/list-lead-lists).

## Create Lead



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "first_name": "Ava",
  "list_key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helloLeads/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "first_name": "Ava",
    "list_key": "string"
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
      "info": {},
      "lead_id": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helloLeads/latest/actions/create-lead).
