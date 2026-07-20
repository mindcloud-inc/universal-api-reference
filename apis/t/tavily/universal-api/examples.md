# Tavily Universal API Examples

These examples use the MindCloud API key and Tavily connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Web

Finds web search results in Tavily by query.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tavily/latest/actions/search-web?${params}`, {
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
      "answer": "string",
      "auto_parameters": {},
      "follow_up_questions": [
        "string"
      ],
      "images": [
        {}
      ],
      "query": "string",
      "request_id": "string",
      "response_time": 1,
      "results": [
        {}
      ],
      "usage": {}
    }
  ],
  "meta": {}
}
```

See the full [Search Web action reference](actions/search-web.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tavily/latest/actions/search-web).

## Create Research Task

Creates a research task in Tavily.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tavily/latest/actions/create-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tavily/latest/actions/create-research-task', {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "input": "string",
      "model": "string",
      "request_id": "string",
      "response_time": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Research Task action reference](actions/create-research-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tavily/latest/actions/create-research-task).
