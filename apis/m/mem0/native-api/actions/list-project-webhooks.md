# List Project Webhooks with Mem0

Retrieves project webhooks from Mem0.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/webhooks/projects/:project_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [List Project Webhooks](https://docs.mem0.ai/api-reference/webhook/get-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Mem0 project ID from the webhook resource path. |
