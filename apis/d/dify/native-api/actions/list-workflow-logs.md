# List Workflow Logs with Dify

Retrieves workflow logs from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/logs`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [List Workflow Logs](https://docs.dify.ai/api-reference/workflow-runs/list-workflow-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return. |
| `keyword` | query | `string` | no | Keyword filter for workflow logs. |
| `status` | query | `string` | no | Workflow run status filter. |
| `created_at__before` | query | `string` | no | Return logs created before this timestamp. |
| `created_at__after` | query | `string` | no | Return logs created after this timestamp. |
| `created_by_end_user_session_id` | query | `string` | no | Filter by end-user session ID. |
| `created_by_account` | query | `string` | no | Filter by creator account. |
