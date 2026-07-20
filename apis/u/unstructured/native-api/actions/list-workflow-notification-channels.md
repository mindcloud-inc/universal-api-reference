# List Workflow Notification Channels with Unstructured

Retrieves workflow notification channels from Unstructured.

## Endpoint

- **Method:** `GET`
- **Path:** `/workflows/:workflow_id/notifications/channels`
- **Base URL:** `https://platform.unstructuredapp.io/api/v1`
- **Official documentation:** [List Workflow Notification Channels](https://docs.unstructured.io/api-reference/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id` | path | `string` | yes | Workflow ID. |
| `channel_type` | query | `string` | no | Filter by channel type. |
