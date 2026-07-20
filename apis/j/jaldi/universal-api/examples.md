# Jaldi Universal API Examples

These examples use the MindCloud API key and Jaldi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Leads

Retrieves leads from Jaldi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/list-leads?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "lastName": "Chen",
      "notes": "string",
      "phone": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Leads action reference](actions/list-leads.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jaldi/latest/actions/list-leads).

## Create Lead

Creates a new lead in Jaldi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "firstName": "Ava",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jaldi/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "firstName": "Ava",
    "phone": "string"
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
      "response": {
        "message": "string",
        "status_code": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Lead action reference](actions/create-lead.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jaldi/latest/actions/create-lead).
