# SEA-LION AI Playground Universal API Examples

These examples use the MindCloud API key and SEA-LION AI Playground connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Models



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/list-models?${params}`, {
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

See the full [List Models action reference](actions/list-models.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sEALIONAIPlaygroundAPI/latest/actions/list-models).

## Create Chat Completion



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "messages[]": [
    {}
  ],
  "messages[].content": "string",
  "messages[].role": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "messages[]": [{}],
    "messages[].content": "string",
    "messages[].role": "string"
  })
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

See the full [Create Chat Completion action reference](actions/create-chat-completion.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sEALIONAIPlaygroundAPI/latest/actions/create-chat-completion).
