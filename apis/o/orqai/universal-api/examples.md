# Orq.ai Universal API Examples

These examples use the MindCloud API key and Orq.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves a list of available models from Orq.ai.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orqai/latest/actions/list-models?${params}`, {
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
      "data": [
        {
          "created": 1,
          "id": "string",
          "type": "string"
        }
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orqai/latest/actions/list-models).

## Create Agent

Creates a new agent in Orq.ai.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/orqai/latest/actions/create-agent', {
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
      "created": "string",
      "description": "string",
      "engine": "string",
      "instructions": "string",
      "key": "string",
      "model": {
        "id": "string"
      },
      "path": "string",
      "role": "string",
      "status": "string",
      "type": "string",
      "updated": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Agent action reference](actions/create-agent.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/orqai/latest/actions/create-agent).
