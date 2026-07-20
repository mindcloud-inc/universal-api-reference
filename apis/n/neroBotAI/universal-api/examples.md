# NeroBot AI Universal API Examples

These examples use the MindCloud API key and NeroBot AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Query AI Task Result

Retrieves an AI task result from NeroBot AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/query-ai-task-result?${params}`, {
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
      "result": {
        "output": "string"
      },
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Query AI Task Result action reference](actions/query-ai-task-result.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neroBotAI/latest/actions/query-ai-task-result).

## Animate Face

Creates a face animation task in NeroBot AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/animate-face" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/neroBotAI/latest/actions/animate-face', {
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
      "result": {
        "output": "string"
      },
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Animate Face action reference](actions/animate-face.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/neroBotAI/latest/actions/animate-face).
