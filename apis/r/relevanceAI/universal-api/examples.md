# Relevance AI Universal API Examples

These examples use the MindCloud API key and Relevance AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tools



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/list-tools?${params}`, {
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
      "description": "string",
      "is_hidden": true,
      "project": "string",
      "public": true,
      "studio_id": "string",
      "title": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Tools action reference](actions/list-tools.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/relevanceAI/latest/actions/list-tools).

## Add Tool to Agent



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/add-tool-to-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "existingActions": {},
  "toolId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/relevanceAI/latest/actions/add-tool-to-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "existingActions": {},
    "toolId": "string"
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
      "agent_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Tool to Agent action reference](actions/add-tool-to-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/relevanceAI/latest/actions/add-tool-to-agent).
