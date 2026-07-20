# Comfy.ICU: Get Run Status

Retrieves a workflow run status from Comfy.ICU.

```
GET https://connect.mindcloud.co/v1/universal/comfyICU/latest/actions/get-run-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Comfy.ICU `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workflowId` | string | yes | Comfy.ICU workflow ID from the workflow page or API code snippet. Example: `6bAK1X_Y7QERnV30MZdo2`. |
| `runId` | string | yes | Run ID returned by the Run Workflow action. Example: `APCmAT2lf8O6sAgk2Svf2`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accelerator` | string | GPU accelerator used for the run. |
| `api_key_id` | string | Comfy.ICU API key ID associated with the run. |
| `client_agent` | string | Client agent that started the run, when available. |
| `completed_at` | date | Timestamp when execution completed. |
| `created_at` | date | Timestamp when the run was created. |
| `data` | object | Request data associated with the run, including the submitted prompt. |
| `deleted_at` | date | Timestamp when the run was deleted, when applicable. |
| `device` | string | Device used to run the workflow. |
| `download_count` | number | Number of downloads for run outputs. |
| `error` | object | Error details when the run fails. |
| `files` | object | Input files associated with the run. |
| `id` | string | Comfy.ICU run ID. |
| `is_nsfw` | boolean | Whether the run is marked as not safe for work. |
| `kind` | string | Run type, such as comfyui. |
| `name` | string | Run name when one is available. |
| `output` | array<object> | Generated output file objects returned after the run completes. |
| `parent_run_id` | string | Parent run ID when this run is derived from another run. |
| `parent_workflow_id` | string | Parent workflow ID when this run is derived from another workflow. |
| `project_id` | number | Comfy.ICU project ID for the run. |
| `retry_count` | number | Number of retries for this run. |
| `run_time` | number | Run duration in milliseconds. |
| `started_at` | date | Timestamp when execution started. |
| `status` | string | Run status such as QUEUED, STARTED, COMPLETED, or ERROR. |
| `tags` | array<string> | Tags associated with the run. |
| `updated_at` | date | Timestamp when the run was last updated. |
| `user` | object | User object associated with the run. |
| `user_id` | string | Comfy.ICU user ID associated with the run. |
| `view_count` | number | Number of views for the run. |
| `visibility` | string | Visibility setting for the run. |
| `webhook` | string | Webhook URL associated with the run, when provided. |
| `workflow_id` | string | Workflow ID associated with this run. |

## Native endpoint

Through the native Comfy.ICU API, this operation is `GET /api/v1/workflows/:workflow_id/runs/:run_id` (base URL `https://comfy.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-run-status.md) for the provider-specific parameters and requirements.

