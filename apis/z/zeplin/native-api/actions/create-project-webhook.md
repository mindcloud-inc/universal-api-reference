# Create Project Webhook with Zeplin

Creates a new project webhook in Zeplin.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{project_id}/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Create Project Webhook](https://docs.zeplin.dev/reference/createprojectwebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
| `url` | body | `string` | yes | The URL of the webhook |
| `name` | body | `string` | yes | The name of the webhook |
| `secret` | body | `string` | yes | The secret to be used to generate signatures for webhook requests |
| `status` | body | `object` | yes | The status of the webhook |
| `events[]` | body | `array<string>` | yes | The events of the webhook |
