# ProxyAPI Universal API Examples

These examples use the MindCloud API key and ProxyAPI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models

Retrieves available models from ProxyAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/list-models?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proxyAPI/latest/actions/list-models).

## Create Chat Completion

Creates a chat completion in ProxyAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "openrouter/openrouter/free",
  "messages[0].content": "Say hello in five words."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/proxyAPI/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "openrouter/openrouter/free",
    "messages[0].content": "Say hello in five words."
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
      "provider": "string",
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Chat Completion action reference](actions/create-chat-completion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/proxyAPI/latest/actions/create-chat-completion).
