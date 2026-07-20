# Tinq.ai Universal API Examples

These examples use the MindCloud API key and Tinq.ai connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspace



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/get-workspace?${params}`, {
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

See the full [Get Workspace action reference](actions/get-workspace.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinqai/latest/actions/get-workspace).

## Enhance Prompt



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/enhance-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": "string",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/enhance-prompt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": "string",
    "prompt": "string"
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

See the full [Enhance Prompt action reference](actions/enhance-prompt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tinqai/latest/actions/enhance-prompt).
