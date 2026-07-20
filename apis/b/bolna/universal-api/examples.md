# Bolna Universal API Examples

These examples use the MindCloud API key and Bolna connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Details

Retrieves your Bolna account details and usage limits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details?${params}`, {
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
      "bypassCompliance": true,
      "concurrency": {},
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "pricing": {},
      "tierPlan": "string",
      "wallet": 1
    }
  ],
  "meta": {}
}
```

See the full [Get User Details action reference](actions/get-user-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bolna/latest/actions/get-user-details).

## Create Agent

Creates a new voice AI agent in Bolna.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentConfig": {},
  "agentPrompts": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bolna/latest/actions/create-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentConfig": {},
    "agentPrompts": {}
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
      "agentId": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bolna/latest/actions/create-agent).
