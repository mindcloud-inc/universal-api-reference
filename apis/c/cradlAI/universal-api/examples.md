# Cradl AI Universal API Examples

These examples use the MindCloud API key and Cradl AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agents

Retrieves all agents from Cradl AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/list-agents?${params}`, {
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
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "metadata": {},
      "name": "Ava Chen",
      "resourceIds": [
        "string"
      ],
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Agents action reference](actions/list-agents.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cradlAI/latest/actions/list-agents).

## Create Agent

Creates a new agent in Cradl AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cradlAI/latest/actions/create-agent', {
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
      "agentId": "string",
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "metadata": {},
      "name": "Ava Chen",
      "resourceIds": [
        "string"
      ],
      "updatedBy": "string",
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cradlAI/latest/actions/create-agent).
