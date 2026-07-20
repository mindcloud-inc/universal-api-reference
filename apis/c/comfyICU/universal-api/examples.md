# Comfy.ICU Universal API Examples

These examples use the MindCloud API key and Comfy.ICU connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Run Status

Retrieves a workflow run status from Comfy.ICU.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/get-run-status?connectionId=$CONNECTION_ID&workflowId=6bAK1X_Y7QERnV30MZdo2&runId=APCmAT2lf8O6sAgk2Svf2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workflowId": "6bAK1X_Y7QERnV30MZdo2",
  "runId": "APCmAT2lf8O6sAgk2Svf2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/get-run-status?${params}`, {
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
      "accelerator": "string",
      "api_key_id": "string",
      "client_agent": "string",
      "completed_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "data": {},
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "device": "string",
      "download_count": 1,
      "error": {},
      "files": {},
      "id": "string",
      "is_nsfw": true,
      "kind": "string",
      "name": "Ava Chen",
      "output": [
        {}
      ],
      "parent_run_id": "string",
      "parent_workflow_id": "string",
      "project_id": 1,
      "retry_count": 1,
      "run_time": 1,
      "started_at": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "tags": [
        "string"
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user": {},
      "user_id": "string",
      "view_count": 1,
      "visibility": "string",
      "webhook": "https://example.com",
      "workflow_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Run Status action reference](actions/get-run-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comfyICU/latest/actions/get-run-status).

## Run Workflow

Creates a new workflow run in Comfy.ICU.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/run-workflow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workflowId": "6bAK1X_Y7QERnV30MZdo2",
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/run-workflow', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workflowId": "6bAK1X_Y7QERnV30MZdo2",
    "prompt": "string"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Run Workflow action reference](actions/run-workflow.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/comfyICU/latest/actions/run-workflow).
