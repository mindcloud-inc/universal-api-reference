# DeepSeek Universal API Examples

These examples use the MindCloud API key and DeepSeek connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/list-models?${params}`, {
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
      "id": "string",
      "object": "string",
      "ownedBy": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepSeek/latest/actions/list-models).

## Create Chat Completion



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "deepseek-chat or deepseek-reasoner",
  "messages[]": "[object Object]",
  "messages[].role": "assistant",
  "messages[].content": "string",
  "tools[].type": "function",
  "tools[].function": {},
  "tools[].function.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/deepSeek/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "deepseek-chat or deepseek-reasoner",
    "messages[]": "[object Object]",
    "messages[].role": "assistant",
    "messages[].content": "string",
    "tools[].type": "function",
    "tools[].function": {},
    "tools[].function.name": "Ava Chen"
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
        {
          "finishReason": "string",
          "index": 1,
          "message": {
            "content": "string",
            "reasoningContent": "string",
            "role": "string",
            "toolCalls": [
              {
                "function": {
                  "arguments": "string",
                  "name": "Ava Chen"
                },
                "id": "string",
                "type": "string"
              }
            ]
          }
        }
      ],
      "created": 1,
      "id": "string",
      "model": "string",
      "object": "string",
      "systemFingerprint": "string",
      "usage": {
        "completionTokens": 1,
        "completionTokensDetails": {
          "reasoningTokens": 1
        },
        "promptCacheHitTokens": 1,
        "promptCacheMissTokens": 1,
        "promptTokens": 1,
        "totalTokens": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Chat Completion action reference](actions/create-chat-completion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/deepSeek/latest/actions/create-chat-completion).
