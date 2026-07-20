# Leap AI Universal API Examples

These examples use the MindCloud API key and Leap AI connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workflow Run

Retrieves a workflow run from Leap AI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run?connectionId=$CONNECTION_ID&workflowRunId=runv2_8R8jNYkpBVLI4FqCJiJ5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowRunId": "runv2_8R8jNYkpBVLI4FqCJiJ5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/get-workflow-run?${params}`, {
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
      "created_at": "string",
      "error": "string",
      "id": "string",
      "result": {},
      "status": "string",
      "version_id": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Workflow Run action reference](actions/get-workflow-run.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leapAI/latest/actions/get-workflow-run).

## Run Workflow

Runs a published workflow in Leap AI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "wkfv2_bZNg4zPR44mA"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leapAI/latest/actions/run-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "wkfv2_bZNg4zPR44mA"
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
      "created_at": "string",
      "error": "string",
      "id": "string",
      "result": {},
      "status": "string",
      "version_id": "string",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Run Workflow action reference](actions/run-workflow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/leapAI/latest/actions/run-workflow).
