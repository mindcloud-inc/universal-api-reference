# Update Project Webhook with Zeplin

Updates an existing project webhook in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{project_id}/webhooks/{webhook_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Project Webhook](https://docs.zeplin.dev/reference/updateprojectwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `webhook_id` | path | `string` | yes | Webhook id |
| `url` | body | `string` | yes | The URL of the webhook |
| `name` | body | `string` | yes | The name of the webhook |
| `secret` | body | `string` | yes | The secret to be used to generate signatures for webhook requests |
| `status` | body | `string` | yes | The status of the webhook |
| `events[]` | body | `array<string>` | yes | The events of the webhook |
