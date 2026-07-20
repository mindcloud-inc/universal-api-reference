# Perplexity Universal API Examples

These examples use the MindCloud API key and Perplexity connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available models from Perplexity.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/list-models?${params}`, {
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
          "object": "string",
          "owned_by": "string"
        }
      ],
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/perplexity/latest/actions/list-models).

## Create Agent Response

Creates an agent response in Perplexity.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-agent-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/perplexity/latest/actions/create-agent-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string"
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
      "created_at": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "output": [
        {
          "content": [
            {
              "text": "string",
              "type": "string"
            }
          ],
          "role": "string",
          "type": "string"
        }
      ],
      "status": "string",
      "usage": {
        "input_tokens": 1,
        "output_tokens": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Agent Response action reference](actions/create-agent-response.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/perplexity/latest/actions/create-agent-response).
