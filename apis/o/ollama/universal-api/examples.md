# Ollama Universal API Examples

These examples use the MindCloud API key and Ollama connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available models from Ollama.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ollama/latest/actions/list-models?${params}`, {
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
      "models": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ollama/latest/actions/list-models).

## Create Anthropic Message

Creates an Anthropic-compatible message in Ollama.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-anthropic-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "maxTokens": 1,
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ollama/latest/actions/create-anthropic-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "maxTokens": 1,
    "messages[]": [{}]
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
      "content": [
        {}
      ],
      "id": "string",
      "model": "string",
      "role": "string",
      "stopReason": "string",
      "type": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Anthropic Message action reference](actions/create-anthropic-message.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ollama/latest/actions/create-anthropic-message).
