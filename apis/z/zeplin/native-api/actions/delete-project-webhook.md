# Delete Project Webhook with Zeplin

Deletes an existing project webhook from Zeplin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/{project_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Delete Project Webhook](https://docs.zeplin.dev/reference/deleteprojectwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `webhook_id` | path | `string` | yes | Webhook id |
