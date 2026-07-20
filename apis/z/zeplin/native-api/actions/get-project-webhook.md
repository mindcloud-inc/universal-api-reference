# Get Project Webhook with Zeplin

Retrieves a project webhook from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Get Project Webhook](https://docs.zeplin.dev/reference/getprojectwebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `webhook_id` | path | `string` | yes | Webhook id |
