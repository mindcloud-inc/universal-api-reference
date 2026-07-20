# Minimax Universal API Examples

These examples use the MindCloud API key and Minimax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Files

Retrieves files from Minimax.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files?connectionId=$CONNECTION_ID&purpose=t2a_async_input" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purpose": "t2a_async_input"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/minimax/latest/actions/list-files?${params}`, {
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
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Files action reference](actions/list-files.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minimax/latest/actions/list-files).

## Compatible Anthropic Messages



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/minimax/latest/actions/compatible-anthropic-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "maxTokens": "32",
  "messages[]": [
    {}
  ],
  "model": "MiniMax-M2.7"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/minimax/latest/actions/compatible-anthropic-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "maxTokens": "32",
    "messages[]": [{}],
    "model": "MiniMax-M2.7"
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
      "base_resp": {
        "status_code": 1,
        "status_msg": "string"
      },
      "choices": {},
      "created": 1,
      "id": "string",
      "input_sensitive": true,
      "input_sensitive_type": 1,
      "model": "string",
      "object": "string",
      "output_sensitive": true,
      "output_sensitive_int": 1,
      "output_sensitive_type": 1,
      "usage": {
        "total_characters": 1,
        "total_tokens": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Compatible Anthropic Messages action reference](actions/compatible-anthropic-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/minimax/latest/actions/compatible-anthropic-messages).
