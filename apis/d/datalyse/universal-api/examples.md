# Datalyse Universal API Examples

These examples use the MindCloud API key and Datalyse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get All Agents

Retrieves all company agents from Datalyse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/get-all-agents?${params}`, {
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
      "agentId": "string",
      "avatar": "string",
      "email": "ava@example.com",
      "language": "string",
      "lastname": "Chen",
      "name": "Ava Chen",
      "phone": "string",
      "role": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get All Agents action reference](actions/get-all-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datalyse/latest/actions/get-all-agents).

## Add Note To Company

Adds a note to a company in Datalyse.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/add-note-to-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyLeadId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datalyse/latest/actions/add-note-to-company', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyLeadId": "string",
    "text": "string"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Note To Company action reference](actions/add-note-to-company.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/datalyse/latest/actions/add-note-to-company).
