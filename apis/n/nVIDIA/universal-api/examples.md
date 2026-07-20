# NVIDIA Universal API Examples

These examples use the MindCloud API key and NVIDIA connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available models from NVIDIA.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/list-models?${params}`, {
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
      "created": 1,
      "id": "string",
      "object": "string",
      "owned_by": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nVIDIA/latest/actions/list-models).

## Create Chat Completion (abacusai/dracarys-llama-3.1-70b-instruct)

Creates a chat completion in NVIDIA using abacusai/dracarys-llama-3.1-70b-instruct.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nVIDIA/latest/actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct', {
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
      "choices": [
        {}
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Chat Completion (abacusai/dracarys-llama-3.1-70b-instruct) action reference](actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/nVIDIA/latest/actions/create-chat-completion-abacusai-dracarys-llama-3-1-70b-instruct).
