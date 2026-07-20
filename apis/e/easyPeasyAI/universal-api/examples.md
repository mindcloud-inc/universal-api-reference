# Easy-Peasy.AI Universal API Examples

These examples use the MindCloud API key and Easy-Peasy.AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Presets

Retrieves text generation presets from Easy-Peasy.AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/list-presets?${params}`, {
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

See the full [List Presets action reference](actions/list-presets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyPeasyAI/latest/actions/list-presets).

## Chat Completions

Creates a chat completion in Easy-Peasy.AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/chat-completions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyPeasyAI/latest/actions/chat-completions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}]
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

See the full [Chat Completions action reference](actions/chat-completions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyPeasyAI/latest/actions/chat-completions).
