# 1minAI Universal API Examples

These examples use the MindCloud API key and 1minAI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Chat with AI

Creates an AI chat response in 1minAI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "prompt": "Explain quantum computing in simple terms"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minAI/latest/actions/chat-with-ai', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "prompt": "Explain quantum computing in simple terms"
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
      "aiRecord": {},
      "temporaryUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Chat with AI action reference](actions/chat-with-ai.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minAI/latest/actions/chat-with-ai).
