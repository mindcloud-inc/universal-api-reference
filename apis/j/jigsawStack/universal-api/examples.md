# JigsawStack Universal API Examples

These examples use the MindCloud API key and JigsawStack connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Search Suggestions



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions?connectionId=$CONNECTION_ID&query=What%20is%20the%20capital" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "What is the capital"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/get-search-suggestions?${params}`, {
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
      "_usage": {},
      "log_id": "string",
      "success": true,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Search Suggestions action reference](actions/get-search-suggestions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jigsawStack/latest/actions/get-search-suggestions).

## Create Prompt



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/create-prompt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jigsawStack/latest/actions/create-prompt', {
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
      "_usage": {},
      "log_id": "string",
      "optimized_prompt": "string",
      "prompt_engine_id": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Prompt action reference](actions/create-prompt.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jigsawStack/latest/actions/create-prompt).
