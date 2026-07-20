# Automate Sales CRM Universal API Examples

These examples use the MindCloud API key and Automate Sales CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Create New Lead V2

Creates a new lead in Automate Sales CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/automateSalesCRM/latest/actions/create-new-lead-v2', {
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
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create New Lead V2 action reference](actions/create-new-lead-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/automateSalesCRM/latest/actions/create-new-lead-v2).
