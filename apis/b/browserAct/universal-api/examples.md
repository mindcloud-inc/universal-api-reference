# BrowserAct Universal API Examples

These examples use the MindCloud API key and BrowserAct connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Official Workflow Templates

Retrieves official workflow templates from BrowserAct.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/list-official-workflow-templates?${params}`, {
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
      "detailUrl": "https://example.com",
      "name": "Ava Chen",
      "recommendDesc": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Official Workflow Templates action reference](actions/list-official-workflow-templates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserAct/latest/actions/list-official-workflow-templates).

## Cancel Running Task

Updates a running task in BrowserAct to cancel execution.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/cancel-running-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserAct/latest/actions/cancel-running-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
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

See the full [Cancel Running Task action reference](actions/cancel-running-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/browserAct/latest/actions/cancel-running-task).
