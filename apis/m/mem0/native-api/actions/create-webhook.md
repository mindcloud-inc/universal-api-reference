# Create Webhook with Mem0

Creates a new webhook in Mem0.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/webhooks/projects/:project_id/`
- **Base URL:** `https://api.mem0.ai`
- **Official documentation:** [Create Webhook](https://docs.mem0.ai/api-reference/webhook/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Mem0 project ID from the webhook resource path. |
