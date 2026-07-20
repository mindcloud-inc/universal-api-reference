# Toolhouse Universal API Examples

These examples use the MindCloud API key and Toolhouse connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Agent Runs



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/list-agent-runs?${params}`, {
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
      "bundle": "string",
      "callback_url": "https://example.com",
      "chat_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "schedule_id": "string",
      "status": "string",
      "toolhouse_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vars": {}
    }
  ],
  "meta": {}
}
```

See the full [List Agent Runs action reference](actions/list-agent-runs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toolhouse/latest/actions/list-agent-runs).

## Continue Agent Run



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/continue-agent-run" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "runId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toolhouse/latest/actions/continue-agent-run', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "runId": "string"
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
      "bundle": "string",
      "callback_url": "https://example.com",
      "chat_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "error": "string",
      "id": "string",
      "schedule_id": "string",
      "status": "string",
      "toolhouse_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "vars": {}
    }
  ],
  "meta": {}
}
```

See the full [Continue Agent Run action reference](actions/continue-agent-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toolhouse/latest/actions/continue-agent-run).
