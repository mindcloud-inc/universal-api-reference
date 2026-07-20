# Shuffler Universal API Examples

These examples use the MindCloud API key and Shuffler connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Apps

Retrieves apps from Shuffler.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/list-apps?${params}`, {
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
      "activated": true,
      "appVersion": "string",
      "id": "string",
      "name": "Ava Chen",
      "verified": true
    }
  ],
  "meta": {}
}
```

See the full [List Apps action reference](actions/list-apps.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shuffler/latest/actions/list-apps).

## Abort Workflow Execution

Aborts a workflow execution in Shuffler.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/abort-workflow-execution" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "executionId": "string",
  "workflowId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/abort-workflow-execution', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "executionId": "string",
    "workflowId": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Abort Workflow Execution action reference](actions/abort-workflow-execution.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shuffler/latest/actions/abort-workflow-execution).
